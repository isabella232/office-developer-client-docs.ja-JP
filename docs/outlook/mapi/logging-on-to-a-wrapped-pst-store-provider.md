---
title: ラップされた PST ストア プロバイダーへのログオン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 1015611fea9b8080ba201855b6a1847c84bdc47a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579650"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーへのログオン

**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップされた PST ストア プロバイダーに MAPI をログオンする前に、ラップされた個人用フォルダー ファイル (PST) ストア プロバイダーを初期化して構成する必要があります。 詳細については、「ラップされた PST ストア [プロバイダーの初期化」を参照してください](initializing-a-wrapped-pst-store-provider.md)。
  
ラップされた PST ストア プロバイダーを初期化して構成した後、2 つのログオン ルーチンを実装する必要があります。 **[IMSProvider::Logon 関数は](imsprovider-logon.md)**、MAPI でラップされた PST ストア プロバイダーにログを記録します。 **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** 関数は、MAPI スプーラーにラップされた PST ストア プロバイダーにログを記録します。 
  
このトピックでは、サンプル ラップ PST ストア プロバイダーのコード例を使用して **、IMSProvider::Logon** 関数と **IMSProvider::SpoolerLogon** 関数を示します。 このサンプルでは、レプリケーション API と組み合わせて使用することを目的としたラップされた PST プロバイダーを実装しています。 サンプル ラップ PST ストア プロバイダーのダウンロードとインストールの詳細については、「サンプル ラップされた PST ストア プロバイダーのインストール [」を参照してください](installing-the-sample-wrapped-pst-store-provider.md)。 レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。
  
MAPI と MAPI スプーラーがラップされた PST ストア プロバイダーにログオンした後、使用する準備が整いました。 詳細については、「Wrapped [PST ストア プロバイダーの使用」を参照してください](using-a-wrapped-pst-store-provider.md)。
  
## <a name="mapi-logon-routine"></a>MAPI ログオン ルーチン

ラップされた PST ストア プロバイダーが初期化された後、ラップされた PST ストアに MAPI にログオンするには **[、IMSProvider::Logon](imsprovider-logon.md)** 関数を実装する必要があります。 この関数は、ユーザー資格情報を検証し、プロバイダーの構成プロパティを取得します。 オフライン ファイル情報  `SetOLFIInOST` **[(OLFI)](olfi.md)** を設定する関数も実装する必要があります。 **OLFI** は、ラップされた PST ストア プロバイダーがオフライン モードで新しいメッセージまたはフォルダーのエントリ ID を割り当てるのに使用する長期 ID 構造のキューです。 最後に **、IMSProvider::Logon** 関数は、MAPI スプーラーとクライアント アプリケーションがパラメーターにログオンできるメッセージ ストア オブジェクトを返  `ppMDB` します。 
  
### <a name="cmsproviderlogon-example"></a>CMSProvider::Logon() の例

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

**IMSProvider::Logon** と同様に、MAPI スプーラーをラップされた PST ストアに記録するには **[、IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** 関数を実装する必要があります。 MAPI スプーラーとクライアント アプリケーションがログオンできるメッセージ ストア オブジェクトがパラメーターに返  `ppMDB` されます。 
  
### <a name="cmsproviderspoolerlogon-example"></a>CMSProvider::SpoolerLogon() の例

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

