---
title: アドレス一覧の解決の順序をプログラムで設定します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f9559afb-8db1-ce72-3e11-9b3d47bb80b6
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: aa1981c365e2a8e81dcd688a32fca25178c7fe52
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577325"
---
# <a name="programmatically-set-the-resolution-order-for-address-lists"></a>アドレス一覧の解決の順序をプログラムで設定します。
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
このトピックには、c++ プログラムを使用してアドレス一覧の受信者に電子メールでメッセージおよび会議出席依頼に出席者は、解決の順序を設定するコード サンプルが含まれています。
  
MAPI の各プロファイルは、複数のアドレス一覧をサポートできるし、自身のコンテナーで、それぞれのアドレス一覧が存在します。 MAPI には、名前解決に使用されるプロファイルに新しい検索パスを設定できるようにするインターフェイスで、 **[SetSearchPath](http://support.microsoft.com/kb/292590)** メソッドがサポートされています。 **IAddrBook::SetSearchPath**メソッドを使用するには、目的の順序に関連するアドレス帳のコンテナーを保持している**[SRowSet](srowset.md)** 配列で、目的の解像度の順序を定義する必要は、 *lpSearchPath*として、配列を指定 パラメーターです。 **SRowSet**配列の各エントリの最初のプロパティは、対応するアドレス帳の**[PR_ENTRYID](pidtagentryid-canonical-property.md)** プロパティである必要があります。 
  
コード サンプルは、次の手順で、解決の順序を設定します。
  
1. 初期化`numANR`が一致するコンテナーの数に解決の順序で、目的のアドレス一覧の名前を指定し、`ANROrder`の配列。 
    
2. **生じます**関数を使用して MAPI を初期化します。 
    
3.  MAPI にログオンし、プロファイルを選択することができます。 
    
4.  現在のセッションからアドレス帳へのポインターを取得します。 
    
5. アドレス帳を開きます。
    
6. アドレス帳のルート コンテナーを開きます。
    
7. ルートのアドレス帳コンテナーの階層テーブルを開きます。
    
8. 階層の一連のアドレス帳コンテナーを取得します。
    
9. 目的のアドレス一覧の名前を比較することで、目的のアドレス一覧のエントリ Id を探します`ANROrder`アドレス帳の階層内の既存の名前にします。 
    
10. **SRowSet**配列に適切なエントリ Id を設定`pNewRows`。
    
11. 呼び出し、渡します`pNewRows`検索パスを設定するのには**IAddrBook::SetSearchPath**に*lpSearchPath*のパラメーターとしてします。 
    
12. 内部バッファーとポインターをクリーンアップします。
    
13. MAPI からログオフします。
    
14. Uninitalizes MAPI です。
    
このコード サンプルを使用して、Microsoft Office Outlook の既定のインストールで使用可能なアドレス一覧:**すべての連絡先**、**すべてのグループ**、および**連絡先**です。 Outlook が起動し、初期化済みのプロファイルで実行している後は、サンプルを実行する必要があります。 サンプルの 1 つの言語に含まれる名前と動作 (たとえば、すべての名前は英語で)。 多言語展開では、英語以外の Outlook を実行してユーザーにローカライズされた**連絡先**フォルダーなどの作業には向いていません。 
  
```cpp
#include "stdafx.h" 
#include <mapix.h> 
#include <mapiguid.h> 
#include <mapiutil.h> 
#include <mapidefs.h> 
#include <stdio.h> 
#include <conio.h> 
 
//Number of address lists to resolve against 
const int numANR = 3; 
WCHAR *ANROrder[numANR] = {_T("All Contacts"), _T("All Groups"), _T("Contacts")}; 
UINT  numContainersFound [numANR] = {0}; 
 
// Temporary structure to allocate buffer in MAPI. This will be used as a parent buffer to free space later. 
LPVOID tempLink; 
 
// Forward declaration of helper function to copy binary data 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent); 
 
void main() 
{ 
    // MAPI address book and session variables 
    HRESULT       hRes = S_OK;            // Result code returned from MAPI calls. 
    LPMAPISESSION lpSession = NULL;   // Pointer to MAPI session. 
    LPADRBOOK     lpAddrBook = NULL;  // Pointer to Address Book. 
 
    // Counters 
    ULONG         i = 0;                  // Index counter 
    ULONG         j = 0;                  // Index counter 
 
    // Used for querying hierarchy 
    ULONG                                   ulObjType = 0L;      // Object type returned by MAPI 
    LPMAPICONTAINER     pIABRoot = NULL;     // Root address book container 
    LPMAPITABLE              pHTable = NULL;      // Holds hierarchy table 
    LPSRowSet        pRows = NULL;        // Pointer to row set. Stores AB Address Lists 
 
    // Used for setting search path 
    LPSRowSet     pNewRows = NULL;        // Pointer to new row set 
    SizedSRowSet  (numANR, NewRows);      // New row set 
    SPropValue    sProps[numANR] = {0};   // Property tag structure 
 
    // Structures contaning MAPI Column Sets required for querying tables 
    enum { 
        abPR_ENTRYID, 
        abPR_DISPLAY_NAME_W, 
        abNUM_COLS}; 
 
    static SizedSPropTagArray(abNUM_COLS,abCols) = { 
        abNUM_COLS, 
        PR_ENTRYID, 
        PR_DISPLAY_NAME_W, 
    }; 
 
    // Initialize MAPI 
    if (FAILED ( hRes = MAPIInitialize(NULL))) goto Exit; 
 
    // Log on to MAPI and allow user to choose profile 
 
    // Note: This uses the current MAPI session if there is one 
    if (FAILED ( hRes = MAPILogonEx(NULL, NULL, NULL, MAPI_LOGON_UI, &lpSession))) goto Exit; 
 
    // Open the Address Book 
    if (FAILED (hRes = lpSession->OpenAddressBook(NULL, NULL, NULL, &lpAddrBook))) goto Cleanup; 
 
    // Open the Address Book Root container 
    if (FAILED (hRes = lpAddrBook -> OpenEntry ( 
        0L,  
        NULL, 
        NULL,  
        0L, 
        &ulObjType, 
        (LPUNKNOWN *) &pIABRoot ))) 
    goto Cleanup; 
 
    // Intentionally allocate 0 bytes. This is used for buffer management. 
    MAPIAllocateBuffer(0L, &tempLink);  
 
    // Make sure there is a Container object 
    // Query hierarchy for containers 
    if ( MAPI_ABCONT == ulObjType ) { 
        // - Call IMAPIContainer::GetHierarchyTable to open the Hierarchy 
        //   table of the root address book container 
        if ( FAILED ( hRes = pIABRoot -> GetHierarchyTable ( CONVENIENT_DEPTH | MAPI_UNICODE, 
            &pHTable ) ) ) 
        goto Cleanup; 
 
        // Get the list of address book containers first 
        if ( FAILED ( hRes = HrQueryAllRows (  
            pHTable, 
            (LPSPropTagArray) &abCols, 
            NULL, 
            NULL, 
            0L, 
            &pRows ) ) ) 
        goto Cleanup; 
 
        // Initialize the structures to set the search order 
        ZeroMemory(&NewRows, numANR * sizeof(SRow)); 
        pNewRows = (LPSRowSet)&NewRows; 
 
        // Set the number of rows you are going to set 
        pNewRows->cRows = numANR; 
 
        // Set the pointers to the structures 
        for (i=0; i<numANR; i++) 
            pNewRows->aRow[i].lpProps = &sProps[i]; 
 
        // Compare the list to the ones that of interest 
        for (i=0; i<pRows->cRows; i++) { 
            if (pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].ulPropTag == PR_DISPLAY_NAME_W) { 
                LPWSTR containerName =  pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].Value.lpszW; 
                for (j=0; j<numANR; j++) 
                    if (!wcscmp (containerName, ANROrder[j])) { 
                        // First check if a container with this name has been found already 
                        if (numContainersFound[j] == 0) { 
                            numContainersFound[j]++; 
                            pNewRows->aRow[j].cValues = 1; 
 
                            // The property being passing is PR_ENTRY_ID 
                            pNewRows->aRow[j].lpProps[0].ulPropTag = PR_ENTRYID; 
 
                            // Copy the binary data over 
                            if (FAILED (hRes = CopySBinary( 
                                &pNewRows->aRow[j].lpProps[0].Value.bin, 
                                &pRows->aRow[i].lpProps[abPR_ENTRYID].Value.bin, 
                                tempLink))) {  
                                    printf ("Fatal Error:Failed to copy entry IDs\n"); 
                                    goto Cleanup; 
                            } 
                         } 
                         // More than 1 container matched the same name 
                         else {  
                             printf ("Fatal Error: Duplicate container found, container name = %s\n", containerName); 
                             goto Cleanup; 
                         } 
                    } 
            } 
        } 
 
        // Only set the search path if all the rows have been found 
        // Check the array for any entries that were blank 
        for (i=0; i< numANR; i++) 
            if (numContainersFound [i] == 0) { 
                printf ("Fatal Error: all containers were not found\n"); 
                goto Cleanup; 
            } 
 
        // Everything is safe to set the search path now 
        if (FAILED (hRes = lpAddrBook->SetSearchPath(0, pNewRows))) {                    
            printf ("Fatal Error: failed to set the search path\n"); 
            goto Cleanup; 
        } 
    } 
 
    Cleanup: 
        MAPIFreeBuffer(tempLink); 
        UlRelease(pHTable); 
        FreeProws(pRows); 
        UlRelease (pIABRoot); 
        UlRelease(lpAddrBook); 
 
        // Log off from MAPI 
        hRes = lpSession->Logoff(NULL, NULL, 0); 
        UlRelease(lpSession); 
 
    Exit: 
        // Uninitialize MAPI 
        MAPIUninitialize(); 
} 
 
///////////////////////////////////////////////////////////// 
//    CopySBinary() 
// 
//    Parameters 
// 
//    Purpose 
//      Allocates a new SBinary and copies psbSrc into it 
// 
 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent) 
{ 
    HRESULT     hRes = S_OK; 
    psbDest->cb = psbSrc->cb; 
 
    if (psbSrc->cb) { 
        if (pParent) 
            hRes = MAPIAllocateMore( 
                 psbSrc->cb, 
                 pParent, 
                 (LPVOID*) &psbDest->lpb); 
        else 
            hRes = MAPIAllocateBuffer( 
                 psbSrc->cb, 
                 (LPVOID*) &psbDest->lpb); 
 
    if (!FAILED(hRes)) 
        CopyMemory(psbDest->lpb,psbSrc->lpb,psbSrc->cb); 
    } 
 
   return hRes; 
} 

```

## <a name="see-also"></a>関連項目

- [Outlook でのアドレス一覧の解決順序の設定について](about-setting-the-resolution-order-for-address-lists-in-outlook.md)

