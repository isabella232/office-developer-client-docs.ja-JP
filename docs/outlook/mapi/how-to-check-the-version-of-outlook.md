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
# <a name="check-the-version-of-outlook"></a><span data-ttu-id="ed198-103">Outlook のバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="ed198-103">Check the version of Outlook</span></span>

<span data-ttu-id="ed198-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed198-p101">�����ł́A�C���X�g�[������Ă���o�[�W������Microsoft Outlook 2013�A Microsoft Outlook 2010�A Microsoft Office Outlook 2007�A�܂���Microsoft Outlook 2003�ꍇ�́A Microsoft Outlook�̃o�[�W�����̃o�[�W��������m�F������Љ�܂��BOutlook�̃o�[�W������m�F����� MAPI �A�v���P�[�V�����Ăяo�� API �v�fOutlook�̎��s���̃o�[�W�����ŃT�|�[�g����Ă��邱�Ƃ�m�F����K�v���ł�B</span><span class="sxs-lookup"><span data-stu-id="ed198-p101">This topic provides a code sample that checks version information of installed versions of Microsoft Outlook if the installed version is Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, or Microsoft Outlook 2003. Checking the version of Outlook is sometimes necessary to ensure that a MAPI application calls API elements that are supported by the currently running version of Outlook.</span></span>

<span data-ttu-id="ed198-p102">���̃R�[�h �T���v���A  `PrintOutlookVersionString`�֐���g�p���āA **MsiProvideQualifiedComponent**�� **MsiGetFileVersion** �AMsi.h �t�@�C���ŁAMicrosoft Windows �\�t�g�E�F�A�J���L�b�g (SDK) �Ő錾����Ă��鐻�i�ł̕������擾���܂��B  `PrintOutlookVersionString`��Outlook�� 64 �r�b�g�ł��C���X�g�[������Ă��邩�ǂ���������u�[���^�ϐ��Ƀ|�C���^�[��Ԃ��܂��B�ꕔ�̃����[�X�ł� Outlook �̃o�[�W�����̕�����̕ʂ̕����̗\���l�ɂ��ẮA [Outlook �̃o�[�W��������m�F������@](https://support.microsoft.com/kb/870929)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ed198-p102">The following code sample,  `PrintOutlookVersionString`, obtains full version strings by using the **MsiProvideQualifiedComponent** and **MsiGetFileVersion** functions, as declared in the Msi.h file in the Microsoft Windows Software Development Kit (SDK).  `PrintOutlookVersionString` also returns a pointer to a Boolean variable that indicates whether a 64-bit version of Outlook is installed. For information about the expected values for the different parts of a version string for some released versions of Outlook, see [How to determine Outlook version information](https://support.microsoft.com/kb/870929).</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="ed198-110">�֘A����</span><span class="sxs-lookup"><span data-stu-id="ed198-110">See also</span></span>

- [<span data-ttu-id="ed198-111">MAPI �v���O���~���O�̊T�v</span><span class="sxs-lookup"><span data-stu-id="ed198-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

