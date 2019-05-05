# FragmentPreference
# ![EditText](https://github.com/JojoBiid/FragmentPreference/blob/master/app/src/main/res/drawable/edit.png)
# ![List](https://github.com/JojoBiid/FragmentPreference/blob/master/app/src/main/res/drawable/list.png)
# ![Screen](https://github.com/JojoBiid/FragmentPreference/blob/master/app/src/main/res/drawable/screen.png)
# ![Intent](https://github.com/JojoBiid/FragmentPreference/blob/master/app/src/main/res/drawable/intent.png)
# ![Parent](https://github.com/JojoBiid/FragmentPreference/blob/master/app/src/main/res/drawable/parent.png)
```
<PreferenceScreen
    xmlns:android="http://schemas.android.com/apk/res/android">
    <PreferenceCategory
        android:key="In_line"
        android:title="@string/In_line">
        <CheckBoxPreference
            android:key="pref_sync"
            android:title="@string/preference"
            android:summary="@string/pre_sum"
            android:defaultValue="false"/>
    </PreferenceCategory>

    <PreferenceCategory
        android:key="Dialog_based"
        android:title="@string/Dialog_based">
        <EditTextPreference
            android:key="edit_pref"
            android:title="@string/Edit_pref"
            android:dialogTitle="@string/Edit_pref1"
            android:summary="@string/pre_sum2"

            />
    </PreferenceCategory>
    <ListPreference
        android:key="pref_syncConnectionType"
        android:title="@string/pref_syncConnectionType"
        android:dialogTitle="@string/pref_syncConnectionType1"
        android:summary="@string/pre_sum1"
        android:entries="@array/languages"
        android:entryValues="@array/languages"

        />
    <PreferenceCategory
        android:key="Launch_pre"
        android:title="@string/Launch_pref">
        <PreferenceScreen android:key="Screen_pref" android:title="@string/Screen_pref" android:summary="@string/pre_sum3">
            <CheckBoxPreference
                android:key="Toggle"
                android:title="@string/Toggle"
                android:summary="@string/pre_sum7"
                android:defaultValue="false"
                />
        </PreferenceScreen>
    </PreferenceCategory>
    <Preference
        android:title="@string/Intent"
        android:summary="@string/pre_sum4">
        <intent
            android:action="android.intent.action.VIEW"      
            android:data="https://www.baidu.com"
            />
    </Preference>
    <PreferenceCategory
        android:key="Attribute"
        android:title="@string/Attribute">
        <CheckBoxPreference
            android:key="parent_pref"
            android:title="@string/Parent"
            android:summary="@string/pre_sum5"
            android:defaultValue="false"
            />
    </PreferenceCategory>
    <CheckBoxPreference
        android:key="child_pref"
        android:title="@string/Child"
        android:summary="@string/pre_sum6"
        android:dependency="parent_pref"
        android:defaultValue="false"/>
</PreferenceScreen>
```
