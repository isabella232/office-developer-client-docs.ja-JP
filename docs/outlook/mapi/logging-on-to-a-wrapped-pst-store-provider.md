---
title: ラップされた PST ストア プロバイダーにログオンしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 0716017788239c22f31007438089118d109010a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570479"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーにログオンしています。

**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI は、ラップされた PST ストア プロバイダーにログオンすることができます、前に初期化し、ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーを構成する必要があります。 詳細については、[ラップの PST ストア プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)を参照してください。
  
初期化し、ラップされた PST ストア プロバイダーを構成した後、2 つのログオン ルーチンを実装する必要があります。 **[IMSProvider::Logon](imsprovider-logon.md)** 関数は、MAPI、ラップされた PST ストア プロバイダーにログオンします。 **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** 関数は、ラップされた PST ストア プロバイダーに MAPI スプーラーによってログオンします。 
  
このトピックでは、 **IMSProvider::Logon**関数および**IMSProvider::SpoolerLogon**関数はサンプル ラップ PST ストア プロバイダーのコード例を使用して説明します。 レプリケーション API と連携して使用するものでは、ラップされた PST プロバイダーを実装します。 ダウンロードとサンプル ラップ PST ストア プロバイダーをインストールする方法の詳細については、「[サンプル ラップ PST ストア プロバイダーをインストールする](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。 レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。
  
MAPI および MAPI スプーラーがログに記録した後にラップされた pst ファイルには、プロバイダーを格納、使用する準備ができてです。 詳細については、「[ラップの PST ストア プロバイダー](using-a-wrapped-pst-store-provider.md)」を参照してください。
  
## <a name="mapi-logon-routine"></a>MAPI ログオン ルーチン

ラップされた PST ストア プロバイダーが初期化された後は、ラップされた PST ストアに、MAPI ログオンを**[IMSProvider::Logon](imsprovider-logon.md)** 関数を実装しなければなりません。 この関数は、ユーザーの資格情報を検証し、プロバイダーの構成のプロパティを取得します。 実装する必要があります、 `SetOLFIInOST` 、オフライン ファイルの情報 (**[OLFI](olfi.md)** ) を設定します。 **OLFI**は、新しいメッセージまたはオフライン モードでのフォルダーのエントリ ID を割り当てるには、ラップされた PST ストア プロバイダーによって使用される ID の長期的な構造体のキューです。 最後に、 **IMSProvider::Logon**関数オブジェクトを返します、メッセージ ストア内に MAPI スプーラーとクライアント アプリケーションがログオンできること、`ppMDB`のパラメーターです。 
  
### <a name="cmsproviderlogon-example"></a>CMSProvider::Logon() の使用例

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a>MAPI スプーラー ログオン ルーチン

**IMSProvider::Logon**と同様に、ラップされた PST ストアに、MAPI スプーラーをログに記録する**[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** 関数を実装する必要があります。 MAPI スプーラーとクライアント アプリケーションがログオンすることができるメッセージ ストア オブジェクトが返され、`ppMDB`のパラメーターです。 
  
### <a name="cmsproviderspoolerlogon-example"></a>CMSProvider::SpoolerLogon() の使用例

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a>関連項目

- [ラップされた PST ストア プロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md) 
- [ラップされた PST ストア プロバイダーのサンプルのインストール](installing-the-sample-wrapped-pst-store-provider.md) 
- [ラップされた PST ストア プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーの使用](using-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

