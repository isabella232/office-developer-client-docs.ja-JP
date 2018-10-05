---
title: Outlook のバージョンを確認します。
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 672fc380-a29b-4e99-9211-949fd5065723
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 0a24ae43c84a0631f355a4d7d8dc98a76519563b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388218"
---
# <a name="check-the-version-of-outlook"></a>Outlook のバージョンを確認します。

**適用対象**: Outlook 2013 | Outlook 2016 
  
�����ł́A�C���X�g�[������Ă���o�[�W������Microsoft Outlook 2013�A Microsoft Outlook 2010�A Microsoft Office Outlook 2007�A�܂���Microsoft Outlook 2003�ꍇ�́A Microsoft Outlook�̃o�[�W�����̃o�[�W��������m�F������Љ�܂��BOutlook�̃o�[�W������m�F����� MAPI �A�v���P�[�V�����Ăяo�� API �v�fOutlook�̎��s���̃o�[�W�����ŃT�|�[�g����Ă��邱�Ƃ�m�F����K�v���ł�B

���̃R�[�h �T���v���A  `PrintOutlookVersionString`�֐���g�p���āA **MsiProvideQualifiedComponent**�� **MsiGetFileVersion** �AMsi.h �t�@�C���ŁAMicrosoft Windows �\�t�g�E�F�A�J���L�b�g (SDK) �Ő錾����Ă��鐻�i�ł̕������擾���܂��B  `PrintOutlookVersionString`��Outlook�� 64 �r�b�g�ł��C���X�g�[������Ă��邩�ǂ���������u�[���^�ϐ��Ƀ|�C���^�[��Ԃ��܂��B�ꕔ�̃����[�X�ł� Outlook �̃o�[�W�����̕�����̕ʂ̕����̗\���l�ɂ��ẮA [Outlook �̃o�[�W��������m�F������@](https://support.microsoft.com/kb/870929)��Q�Ƃ��Ă��������B
  
```cpp
void PrintOutlookVersionString()
{
TCHAR pszOutlookQualifiedComponents[][MAX_PATH] = {
TEXT("{E83B4360-C208-4325-9504-0D23003A74A5}"), // Outlook 2013
TEXT("{1E77DE88-BCAB-4C37-B9E5-073AF52DFD7A}"), // Outlook 2010
TEXT("{24AAE126-0911-478F-A019-07B875EB9996}"), // Outlook 2007
TEXT("{BC174BAD-2F53-4855-A1D5-0D575C19B1EA}")  // Outlook 2003
};
int nOutlookQualifiedComponents = _countof(pszOutlookQualifiedComponents);
int i = 0;
UINT ret = 0;
for (i = 0; i < nOutlookQualifiedComponents; i++)
{
DWORD dwValueBuf = 0;
LPTSTR pszTempPath = NULL;
LPTSTR pszTempVer = NULL;
bool b64 = false;
ret = pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.x64.exe"),
(DWORD) INSTALLMODE_DEFAULT,
NULL,
&dwValueBuf);
if (ERROR_SUCCESS == ret)
{
b64 = true;
}
else
{
ret = pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.exe"),
(DWORD) INSTALLMODE_DEFAULT,
NULL,
&dwValueBuf);
if (ERROR_SUCCESS == ret)
{
b64 = false;
}
}
if (ret == ERROR_SUCCESS)
{
dwValueBuf += 1;
pszTempPath = (LPTSTR) malloc(dwValueBuf * sizeof(TCHAR));
if (pszTempPath != NULL)
{
if (ERROR_SUCCESS == pfnMsiProvideQualifiedComponent(
pszOutlookQualifiedComponents[i],
TEXT("outlook.exe"),
(DWORD) INSTALLMODE_EXISTING,
pszTempPath,
&dwValueBuf))
{
pszTempVer = (LPTSTR) malloc(MAX_PATH * sizeof(TCHAR));
dwValueBuf = MAX_PATH;
if (ERROR_SUCCESS == pfnMsiGetFileVersion(pszTempPath,
pszTempVer,
&dwValueBuf,
NULL,
NULL))
{
printf("Path: %s\nVersion: %s\n64 bit: %s\n", pszTempPath, pszTempVer, b64?_T("true"):_T("false"));
}
}
}
free(pszTempVer);
free(pszTempPath);
}
}
}HRESULT GetOutlookVersionString(LPTSTR* ppszVer, BOOL* pf64Bit)
{
    HRESULT hr = E_FAIL;
    LPTSTR pszTempPath = NULL;
    LPTSTR pszTempVer = NULL;
    TCHAR pszOutlookQualifiedComponents[][MAX_PATH] = {
        TEXT("{E83B4360-C208-4325-9504-0D23003A74A5}"), // Outlook 2013
        TEXT("{1E77DE88-BCAB-4C37-B9E5-073AF52DFD7A}"), // Outlook 2010
        TEXT("{24AAE126-0911-478F-A019-07B875EB9996}"), // Outlook 2007
        TEXT("{BC174BAD-2F53-4855-A1D5-0D575C19B1EA}")  // Outlook 2003
    };
    int nOutlookQualifiedComponents = _countof(pszOutlookQualifiedComponents);
    int i = 0;
    DWORD dwValueBuf = 0;
    UINT ret = 0;
    *pf64Bit = FALSE;
    for (i = 0; i < nOutlookQualifiedComponents; i++)
    {
        ret = MsiProvideQualifiedComponent(
            pszOutlookQualifiedComponents[i],
            TEXT("outlook.x64.exe"),
            (DWORD) INSTALLMODE_DEFAULT,
            NULL,
            &dwValueBuf);
        if (ERROR_SUCCESS == ret) break;
    }
    if (ret != ERROR_SUCCESS)
    {
        for (i = 0; i < nOutlookQualifiedComponents; i++)
        {
            ret = MsiProvideQualifiedComponent(
                pszOutlookQualifiedComponents[i],
                TEXT("outlook.exe"),
                (DWORD) INSTALLMODE_DEFAULT,
                NULL,
                &dwValueBuf);
            if (ERROR_SUCCESS == ret) break;
        }
    }
    else
    {
        *pf64Bit = TRUE;
    }
    if (ret == ERROR_SUCCESS)
    {
        dwValueBuf += 1;
        pszTempPath = (LPTSTR) malloc(dwValueBuf * sizeof(TCHAR));
        if (pszTempPath != NULL)
        {
            if ((ret = MsiProvideQualifiedComponent(
                pszOutlookQualifiedComponents[i],
                TEXT("outlook.exe"),
                (DWORD) INSTALLMODE_EXISTING,
                pszTempPath,
                &dwValueBuf)) != ERROR_SUCCESS)
            {
                goto Error;
            }
            pszTempVer = (LPTSTR) malloc(MAX_PATH * sizeof(TCHAR));
            dwValueBuf = MAX_PATH;
            if ((ret = MsiGetFileVersion(pszTempPath,
                pszTempVer,
                &dwValueBuf,
                NULL,
                NULL))!= ERROR_SUCCESS)
            {
                goto Error;    
            }
            *ppszVer = pszTempVer;
            pszTempVer = NULL;
            hr = S_OK;
        }
    }
Error:
    free(pszTempVer);
    free(pszTempPath);
    return hr;
}

```

## <a name="see-also"></a>�֘A����

- [MAPI �v���O���~���O�̊T�v](mapi-programming-overview.md)

