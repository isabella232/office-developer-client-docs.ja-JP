---
title: ラップされた PST ストア プロバイダーへのログオン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: '最終更新日: 2012 年7月2日'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307820"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーへのログオン

**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップされた pst ストアプロバイダーに MAPI をログオンするには、その前に、ラップされた個人用フォルダーファイル (PST) ストアプロバイダーを初期化して構成する必要があります。 詳細については、「ラップされ[た PST ストアプロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)」を参照してください。
  
ラップされた PST ストアプロバイダーを初期化して構成した後、2つのログオンルーチンを実装する必要があります。 **[IMSProvider:: Logon](imsprovider-logon.md)** 関数は、ラップされた PST ストアプロバイダーに MAPI 上でログ記録します。 **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** 関数は、MAPI スプーラーで、ラップされた PST ストアプロバイダーへのログを記録します。 
  
このトピックでは、サンプルのラップされた PST ストアプロバイダーのコード例を使用して、 **IMSProvider:: Logon**関数と**IMSProvider:: SpoolerLogon**関数を示します。 このサンプルでは、レプリケーション API と共に使用することを目的とした、ラップされた PST プロバイダーを実装しています。 サンプルのラップされた pst ストアプロバイダーのダウンロードとインストールの詳細については、「[サンプルのラップされた pst ストアプロバイダーのインストール](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。 レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。
  
mapi および mapi スプーラーは、ラップされた PST ストアプロバイダーにログオンした後、使用する準備ができています。 詳細については、「ラップされ[た PST ストアプロバイダーの使用](using-a-wrapped-pst-store-provider.md)」を参照してください。
  
## <a name="mapi-logon-routine"></a>MAPI ログオンルーチン

ラップされた pst ストアプロバイダーの初期化後、 **[IMSProvider:: Logon](imsprovider-logon.md)** 関数を実装して、ラップされた pst ストアに MAPI でログオンする必要があります。 この関数は、ユーザーの資格情報を検証し、プロバイダーの構成プロパティを取得します。 また、オフラインファイル情報`SetOLFIInOST` (**[olfi](olfi.md)** ) を設定する関数を実装する必要があります。 **olfi**は、新しいメッセージまたはフォルダーのエントリ ID をオフラインモードで割り当てるために、ラップされた PST ストアプロバイダーが使用する、長期間の ID 構造のキューです。 最後に、 **IMSProvider:: Logon**関数は、MAPI スプーラーおよびクライアントアプリケーションが`ppMDB`パラメーターにログオンできるメッセージストアオブジェクトを返します。 
  
### <a name="cmsproviderlogon-example"></a>cmsprovider:: Logon () の例

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

## <a name="mapi-spooler-logon-routine"></a>MAPI スプーラーログオンルーチン

**IMSProvider:: Logon**と同様に、MAPI スプーラーをラップされた PST ストアに記録するには、 **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** 関数を実装する必要があります。 MAPI スプーラーおよびクライアントアプリケーションがログオンできるメッセージストアオブジェクトは、 `ppMDB`パラメーターで返されます。 
  
### <a name="cmsproviderspoolerlogon-example"></a>cmsprovider:: SpoolerLogon () の例

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

- [ラップされた PST ストアプロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md) 
- [ラップされた PST ストアプロバイダーのサンプルのインストール](installing-the-sample-wrapped-pst-store-provider.md) 
- [ラップされた PST ストアプロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーの使用](using-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

