# 实验四
## PrefereceFragment
### 设置界面
![无法显示](/images/1.jpg)
### EditTextPreference
![无法显示](/images/2.png)
### ListPreference
![无法显示](/images/3.jpg)
### 跳转到另一个PreferenceScreen
![无法显示](/images/4.jpg)
### 启动一个网页
![无法显示](/images/5.jpg)
### 父选项与子选项
![无法显示](/images/6.jpg)
![无法显示](/images/7.jpg)
### 关键代码
```
<PreferenceCategory
        android:title="@string/pref_inline_title"
        android:key="pref_key_storage_settings">
    <CheckBoxPreference
        android:key="pref_sync"
        android:title="@string/pref_sync"
        android:summary="@string/pref_sync_summ"
        android:defaultValue="false" />
    </PreferenceCategory>
    <PreferenceCategory
        android:title="@string/pref_dlgbs_title"
        android:key="pref_key_storage_settings">
    <EditTextPreference
        android:dialogTitle="@string/pref_ed_dlg"
        android:key="editTitlePreference"
        android:title="@string/pref_ed"
        android:summary="@string/pref_ed_summ"
        ></EditTextPreference>
    <ListPreference
        android:key="listPreference"
        android:title="@string/pref_ls"
        android:summary="@string/pref_ls_summ"
        android:entries="@array/list_entries"
        android:entryValues="@array/list_entries_value"
        android:dialogTitle="dialogTitle"
        android:defaultValue="@array/list_entries_value2">
    </ListPreference>
    </PreferenceCategory>
    <PreferenceCategory
        android:title="@string/pref_lnh_title"
        android:key="pref_key_storage_settings">
    <PreferenceScreen
        android:key="pref_sc"
        android:title="@string/pref_sc"
        android:summary="@string/pref_sc_summ"
        android:persistent="false">
        <CheckBoxPreference
            android:key="pref_sc_to"
            android:title="@string/pref_sc_to"
            android:summary="@string/pref_sc_to_summ"
            android:defaultValue="false" />
    </PreferenceScreen>
    <Preference android:title="@string/pref_web_page"
                android:summary="@string/pref_web_page_summ" >
        <intent
            android:action="android.intent.action.VIEW"
            android:data="http://www.baidu.com" />
    </Preference>
    </PreferenceCategory>
    <PreferenceCategory
        android:title="@string/pref_att_title"
        android:key="pref_key_storage_settings">
    <CheckBoxPreference
        android:key="pref_par"
        android:title="@string/pref_par"
        android:summary="@string/pref_par_summ"
        android:defaultValue="false" />
    <CheckBoxPreference
        android:dependency="pref_par"
        android:key="pref_ch"
        android:title="@string/pref_ch"
        android:summary="@string/pref_ch_summ"
        android:defaultValue="false" />
    </PreferenceCategory>
```
