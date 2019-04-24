---
title: ラップされた PST ストア プロバイダーの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: '最終更新日: 2012 年7月3日'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329688"
---
# <a name="using-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーの使用

**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップされた個人用フォルダーファイル (PST) ストアプロバイダーを使用する前に、ラップされた PST ストアプロバイダーを初期化して構成する必要があります。 ラップされた PST ストアプロバイダーを構成した後、mapi および mapi スプーラーがメッセージストアプロバイダーにログオンできるように、関数を実装する必要があります。 ラップされた pst ストアプロバイダーの初期化とログオンの詳細については、「ラップされた pst ストア[プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)と、ラップされた[pst ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)」を参照してください。
  
**[imapisupport:: IUnknown](imapisupportiunknown.md)** インターフェイスは、メッセージストアプロバイダーが一般的に実行するタスクの実装を提供します。 このインターフェイスは、サンプルのラップされた PST ストアプロバイダーが機能するようにラップする必要があります。 **[imapisupport:: openプロファイル](imapisupport-openprofilesection.md)** の各関数には、特別な実装が必要です。 他のすべての関数は、パラメーターを基になるラップされたオブジェクトに渡すことができます。 
  
このトピックでは、サンプルのラップされた PST ストアプロバイダーのコード例を使用して、 **imapisupport:: openプロファイル**の使い方を示します。 このサンプルでは、レプリケーション API と共に使用することを目的とした、ラップされた PST プロバイダーを実装しています。 サンプルのラップされた pst ストアプロバイダーのダウンロードとインストールの詳細については、「[サンプルのラップされた pst ストアプロバイダーのインストール](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。 レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。
  
ラップされた pst ストアプロバイダーの使用が終了したら、ラップされた pst ストアプロバイダーを適切にシャットダウンする必要があります。 詳細については、「ラップされ[た PST ストアプロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)」を参照してください。
  
## <a name="open-profile-section-routine"></a>プロファイルセクションルーチンを開く

**[imapisupport:: openプロファイル](imapisupport-openprofilesection.md)** のセクションは、現在のプロファイルのセクションを開きます。 この関数では、ラップされた PST ストアプロバイダーの実装で、特別な処理を行う必要があります。 `pgNSTGlobalProfileSectionGuid`が要求されると、関数はキャッシュされたプロファイルセクションを返します。 
  
### <a name="csupportopenprofilesection-example"></a>csupport:: openプロファイルの例 () の例

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a>関連項目

- [ラップされた PST ストアプロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーのサンプルのインストール](installing-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストアプロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

