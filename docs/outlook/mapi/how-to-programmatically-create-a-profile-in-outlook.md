---
title: Outlook でプログラムによりプロファイルを作成する
manager: soliver
ms.date: 06/02/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2a8561a9-df09-453a-b415-c45910625870
description: "���̃g�s�b�N�ł́A�v���O������g�p���āA�v���t�@�C�� �I�u�W�F�N�g��emsuid ] �Z�N�V������ MAPI �v���p�e�B��ǉ����� Outlook 2016 �Ńv���t�@�C����X�V������@�ɂ\x82��Đ�����܂��B"
ms.openlocfilehash: 30373bba054e25ad4c3288cbcdfcb1779df93471
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616979"
---
# <a name="programmatically-create-a-profile-in-outlook"></a>Outlook でプログラムによりプロファイルを作成する

**適用対象**: Office 365 |Outlook |Outlook 2016 

���̃g�s�b�N�ł́A�v���O������g�p���āA�v���t�@�C�� �I�u�W�F�N�g�� **emsuid** ] �Z�N�V������ MAPI �v���p�e�B��ǉ����� Outlook 2016 �Ńv���t�@�C����X�V������@�ɂ��Đ�����܂��B 

MAPI�A�ȉ��̎菇�Ɏ�����Ă��� **PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)** �A�v���p�e�B��ݒ肵�āA�v���t�@�C����X�V�ł��܂��B 
  
### <a name="set-the-property-for-outlook-2016"></a>Outlook 2016 �̃v���p�e�B��ݒ肵�܂��B

1. Outlook 2016 �ł́A�v���p�e�B���\������Ă��邱�Ƃ�m�F���܂��B
    
2. [IMAPIProp](https://msdn.microsoft.com/library/cc815525.aspx)�C���^�[�t�F�C�X��g�p����ƁAOutlook �v���t�@�C�� �Z�N�V�����Ɉړ����܂��B 
    
   ����́AOutlook �ō���� MAPI �O���[�o�� �v���t�@�C��] �Z�N�V�������s�v�ɂȂ��� 2010�N�ł́A��ɂ��邽�߂ł��B[�v���t�@�C��] �Z�N�V�������������ɂ́A�v���p�e�B������� PR_EMSMDB_SECTION_UID (0x3D150102)�B�l�́A[�v���t�@�C��] �Z�N�V������ GUID ���A����ȍ~�̎菇�Ŏg�p����o�C�i���`���ŕۑ�����܂��B���̒l��o���Ă����K�v������܂��B 
    
3. **PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W** �v���p�e�B��ǉ����܂��B 
    
4. �X�g�A�� **emsuid** ] �Z�N�V�����ŁA���ׂẴv���o�C�_�[ **0x6641001F** �̃v���p�e�B��ݒ肵�܂��B 
    
5. **PR_DISPLAY_NAME** �v���p�e�B��ݒ肵�܂��B 
    
## <a name="code-example"></a>コード例

```cpp
// CreateProfile.cpp : Defines the entry point for the console application.
//
#include "stdafx.h"
#include <Windows.h>
#include <MAPIX.h>
#include <MAPIUtil.h>
#include <EdkMdb.h>
#include <iostream>
#include <vector>
#include <map>
using namespace std;
#define PR_PROFILE_USER_SMTP_EMAIL_ADDRESS                  PROP_TAG(PT_TSTRING, pidProfileMin+0x41)
#define PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W                PROP_TAG(PT_UNICODE, pidProfileMin+0x41)
#define PR_EMSMDB_SECTION_UID                               PROP_TAG(PT_BINARY, 0x3D15)
#define MAPI_FORCE_ACCESS                                   0x80000
STDMETHODIMP GetGlobalProfileSection(LPSERVICEADMIN lpSvcAdmin, LPMAPIUID lpMapiUid, ULONG ulFlags, LPPROFSECT * lppProfSect);
STDMETHODIMP GetEMSMDBVarProfileSection(LPSERVICEADMIN lpSvcAdmin, LPPROFSECT lpGlobalProfSection, LPPROFSECT * lppProfSect);
std::map<ULONG, LPWSTR> PropValueMap
{
    {
        PR_DISPLAY_NAME_W,
        L"Anthony"
    },
    {
        PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W,
        L"=SMTP:anthony@contoso.com"
    }
};
int _tmain(int argc, _TCHAR* argv[])
{
    HRESULT             hRes = S_OK;            // Result from MAPI calls.
    LPPROFADMIN         lpProfAdmin = NULL;     // Profile Admin object.
    LPSERVICEADMIN      lpSvcAdmin = NULL;      // Service Admin object.
    LPMAPITABLE         lpMsgSvcTable = NULL;   // Table to hold services.
    LPSRowSet           lpSvcRows = NULL;       // Rowset to hold results of table query.
    vector<SPropValue>  rgvals;
    SRestriction        sres;                   // Restriction structure.
    SPropValue          SvcProps;               // Property structure for restriction.
    LPPROFSECT          lpGlobalProfSection = nullptr;
    LPPROFSECT          lpEmsMdbVarProfSect = nullptr;
    SPropValue          spvSmtpAddressW;
    SPropValue          spvDisplayName;
    // This indicates columns we want returned from HrQueryAllRows.
    enum { iSvcName, iSvcUID, cptaSvc };
    SizedSPropTagArray(cptaSvc, sptCols) = { cptaSvc, PR_SERVICE_NAME, PR_SERVICE_UID };
    string ProfileName = "MAPIProfile";
    // Initialize MAPI.
    if (FAILED(hRes = MAPIInitialize(NULL)))
    {
        cout << "Error initializing MAPI.";
        goto error;
    }
    // Get an IProfAdmin interface.
    if (FAILED(hRes = MAPIAdminProfiles(0,              // Flags.
        &lpProfAdmin))) // Pointer to new IProfAdmin.
    {
        cout << "Error getting IProfAdmin interface.";
        goto error;
    }
    // Create a new profile.
    if (FAILED(hRes = lpProfAdmin->CreateProfile((LPTSTR)ProfileName.c_str(),     // Name of new profile.
                                                    nullptr,          // Password for profile.
                                                    0,          // Handle to parent window.
                                                    0)))        // Flags.
    {
        cout << "Error creating profile.";
        goto error;
    }
    // Get an IMsgServiceAdmin interface off of the IProfAdmin interface.
    if (FAILED(hRes = lpProfAdmin->AdminServices((LPTSTR)ProfileName.c_str(),     // Profile that we want to modify.
                                                    nullptr,          // Password for that profile.
                                                    0,          // Handle to parent window.
                                                    0,             // Flags.
                                                    &lpSvcAdmin))) // Pointer to new IMsgServiceAdmin.
    {
        cout << "Error getting IMsgServiceAdmin interface.";
        goto error;
    }
    // Create the new message service for Exchange.
    if (FAILED(hRes = lpSvcAdmin->CreateMsgService("MSEMS",     // Name of service from MAPISVC.INF.
                                                    NULL,        // Display name of service.
                                                    NULL,        // Handle to parent window.
                                                    NULL)))      // Flags.
    {
        cout << "Error creating Exchange message service.";
        goto error;
    }
    // You now have to obtain the entry id for the new service.
    // You can do this by getting the message service table
    // and getting the entry that corresponds to the new service.
    if (FAILED(hRes = lpSvcAdmin->GetMsgServiceTable(0,                 // Flags.
                                                    &lpMsgSvcTable)))  // Pointer to table.
    {
        cout << "Error getting Message Service Table.";
        goto error;
    }
    // Set up restriction to query table.
    sres.rt = RES_CONTENT;
    sres.res.resContent.ulFuzzyLevel = FL_FULLSTRING;
    sres.res.resContent.ulPropTag = PR_SERVICE_NAME;
    sres.res.resContent.lpProp = &SvcProps;
    SvcProps.ulPropTag = PR_SERVICE_NAME;
    SvcProps.Value.lpszA = "MSEMS";
    // Query the table to obtain the entry for the newly created message service.
    if (FAILED(hRes = HrQueryAllRows(lpMsgSvcTable,
                                        (LPSPropTagArray)&sptCols,
                                        &sres,
                                        NULL,
                                        0,
                                        &lpSvcRows)))
    {
        cout << "Error querying table for new message service.";
        goto error;
    }
    ZeroMemory(&spvSmtpAddressW, sizeof(spvSmtpAddressW));
    spvSmtpAddressW.ulPropTag = PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W;
    spvSmtpAddressW.Value.lpszW = PropValueMap[PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W];
    rgvals.push_back(spvSmtpAddressW);
    // Configure the message service by using the previous properties.
    //if (FAILED(hRes = lpSvcAdmin->ConfigureMsgService(
    //                                                  (LPMAPIUID)lpSvcRows->aRow->lpProps[iSvcUID].Value.bin.lpb, // Entry ID of service to configure.
    //                                                  NULL,                                                       // Handle to parent window.
    //                                                  0,                                                          // Flags.
    //                                                  rgvals.size(),                                                          // Number of properties we are setting.
    //                                                  rgvals.data())))                                                    // Pointer to SPropValue array.
    //{
    //  cout << "Error configuring message service.";
    //  goto error;
    //}
    if (FAILED(hRes = GetGlobalProfileSection(
                                                    lpSvcAdmin, 
                                                    (LPMAPIUID)lpSvcRows->aRow->lpProps[iSvcUID].Value.bin.lpb, 
                                                    MAPI_MODIFY, 
                                                    &lpGlobalProfSection)))
    {
        cout << "Error attempting to get the Global Profile Section.";
        goto error;
    }
    if (FAILED(hRes = lpGlobalProfSection->SetProps(
                                                    rgvals.size(),
                                                    rgvals.data(),
                                                    nullptr)))
    {
        cout << "Error attempting to set the smtp address.";
        goto error;
    }
    if (FAILED(hRes = lpGlobalProfSection->SaveChanges(
                                                        KEEP_OPEN_READWRITE)))
    {
        cout << "Error attempting to save after setting the smtp address";
        goto error;
    }
    if (FAILED(hRes = GetEMSMDBVarProfileSection(lpSvcAdmin, lpGlobalProfSection, &lpEmsMdbVarProfSect)))
    {
        goto error;
    }
    ZeroMemory(&spvDisplayName, sizeof(spvDisplayName));
    spvDisplayName.ulPropTag = PR_DISPLAY_NAME_W;
    spvDisplayName.Value.lpszW = PropValueMap[PR_DISPLAY_NAME_W];
    rgvals.push_back(spvDisplayName);
    if (FAILED(hRes = lpEmsMdbVarProfSect->SetProps(
                                                    rgvals.size(),
                                                    rgvals.data(),
                                                    nullptr)))
    {
        cout << "Error call set props on the ems mdb var prof sect using the smtp address";
        goto error;
    }
    if (FAILED(hRes = lpEmsMdbVarProfSect->SaveChanges(
                                                        KEEP_OPEN_READWRITE)))
    {
        cout << "Error attempting to save after setting the smtp address on the ems mdb var prof sect";
        goto error;
    }
cleanup:
    // Clean up
    if (lpEmsMdbVarProfSect) lpEmsMdbVarProfSect->Release();
    if (lpGlobalProfSection) lpGlobalProfSection->Release();
    if (lpSvcRows) FreeProws(lpSvcRows);
    if (lpMsgSvcTable) lpMsgSvcTable->Release();
    if (lpSvcAdmin) lpSvcAdmin->Release();
    if (lpProfAdmin) lpProfAdmin->Release();
    MAPIUninitialize();
    return 0;
error:
    cout << " hRes = 0x" << hex << hRes << dec << endl;
    goto cleanup;
}
STDMETHODIMP GetGlobalProfileSection(LPSERVICEADMIN lpSvcAdmin, LPMAPIUID lpMapiUid, ULONG ulFlags, LPPROFSECT * lppProfSect)
{
    HRESULT         hRes = MAPI_E_CALL_FAILED;
    LPPROFSECT      lpProfSect = nullptr;
    LPPROFSECT      lpEmsMdbVarProfSect = nullptr;
    ULONG           cValues = 0;
    LPSPropValue    lpProps = nullptr;
    SizedSPropTagArray(1, spta) = { 1, { PR_EMSMDB_SECTION_UID } };
    *lppProfSect = nullptr;
    hRes = lpSvcAdmin->OpenProfileSection(lpMapiUid,
        0,
        MAPI_FORCE_ACCESS,
        &lpProfSect);
    if (FAILED(hRes) || lpProfSect == nullptr)
    {
        return hRes;
    }
    hRes = lpProfSect->GetProps((LPSPropTagArray)&spta, 0, &cValues, &lpProps);
    if (FAILED(hRes) || lpProps == nullptr || cValues == 0)
    {
        return hRes;
    }
    if (lpProps[0].ulPropTag != PR_EMSMDB_SECTION_UID)
    {
        hRes = lpProps[0].Value.err;
        goto Cleanup;
    }
    hRes = lpSvcAdmin->OpenProfileSection((LPMAPIUID)lpProps->Value.bin.lpb, 0, ulFlags, &lpEmsMdbVarProfSect);
    if (FAILED(hRes) || lpEmsMdbVarProfSect == nullptr)
    {
        goto Cleanup;
    }
    *lppProfSect = lpEmsMdbVarProfSect;
Cleanup:
    if (lpProps)
    {
        MAPIFreeBuffer(lpProps);
    }
    if (lpProfSect)
    {
        lpProfSect->Release();
    }
    return hRes;
}
STDMETHODIMP GetEMSMDBVarProfileSection(LPSERVICEADMIN lpSvcAdmin, LPPROFSECT lpGlobalProfSection, LPPROFSECT * lppProfSect)
{
    HRESULT hRes = MAPI_E_CALL_FAILED;
    SizedSPropTagArray(1, sptaStoreProviders) = { 1, { PR_STORE_PROVIDERS } };
    ULONG               cValues = 0;
    LPSPropValue        lpProps = nullptr;
    LPPROFSECT          lpProfSect = nullptr;
    if (!lpSvcAdmin || !lpGlobalProfSection || !lppProfSect)
        return E_INVALIDARG;
    *lppProfSect = nullptr;
    if (FAILED(hRes = lpGlobalProfSection->GetProps(
        (LPSPropTagArray)&sptaStoreProviders,
        0,
        &cValues,
        &lpProps)) || cValues == 0 || lpProps == nullptr)
    {
        cout << "Error attempting to get the PR_STORE_PROVIDERS property " << endl;
        goto Cleanup;
    }
    if (lpProps->ulPropTag != sptaStoreProviders.aulPropTag[0])
    {
        hRes = lpProps->Value.err;
        goto Cleanup;
    }
    if (FAILED(hRes = lpSvcAdmin->OpenProfileSection(
        (LPMAPIUID)lpProps->Value.bin.lpb,
        0,
        MAPI_FORCE_ACCESS | MAPI_MODIFY,
        &lpProfSect)) || lpProfSect == nullptr)
    {
        cout << "Could not open the profile section using the PR_STORE_PROVIDERS property " << endl;
        goto Cleanup;
    }
    *lppProfSect = lpProfSect;
Cleanup:
    if (lpProps)
    {
        MAPIFreeBuffer(lpProps);
        lpProps = nullptr;
    }
    return hRes;
}
```

## <a name="use-mfcmapi-to-configure-outlook-profiles"></a>MFCMAPI ��g�p���āAOutlook �v���t�@�C����\������ɂ�

[MFCMAPI](https://mfcmapi.codeplex.com) MAPI �X�g�A Exchange �� Outlook �̖��̒�����e�Ղɂ��āA�J���҂� MAPI �J���̃T�|�[�g��񋟂���ւ̃A�N�Z�X��񋟂��܂��B 
  
## <a name="see-also"></a>関連項目

- [MFCMAPI を使用して Outlook プロファイルを作成する](https://msdn.microsoft.com/library/office/mt723322.aspx)
  

