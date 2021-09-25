---
title: ラップされた PST ストア プロバイダーの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: 7df7e09410d069d53cea57acc49346d0ee74d967
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623902"
---
# <a name="using-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーの使用

**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップされた個人用フォルダー ファイル (PST) ストア プロバイダーを使用する前に、ラップされた PST ストア プロバイダーを初期化して構成する必要があります。 ラップされた PST ストア プロバイダーを構成した後、MAPI と MAPI スプーラーがメッセージ ストア プロバイダーにログオンできるよう、関数を実装する必要があります。 ラップされた PST ストア プロバイダーへの初期化とログオンの詳細については、「ラップされた PST ストア プロバイダーの初期化とラップ [された PST](initializing-a-wrapped-pst-store-provider.md) ストア プロバイダーへのログオン」を [参照してください](logging-on-to-a-wrapped-pst-store-provider.md)。
  
**[IMAPISupport::IUnknown](imapisupportiunknown.md)** インターフェイスは、メッセージ ストア プロバイダーによって一般的に実行されるタスクの実装を提供します。 このインターフェイスは、サンプル ラップされた PST ストア プロバイダーが動作するためにラップする必要があります。 **[IMAPISupport::OpenProfileSection 関数には](imapisupport-openprofilesection.md)** 特別な実装が必要です。 他のすべての関数は、基になるラップされたオブジェクトにパラメーターを渡す可能性があります。 
  
このトピックでは **、IMAPISupport::OpenProfileSection** 関数について、サンプル ラップ PST ストア プロバイダーのコード例を使用して説明します。 このサンプルでは、レプリケーション API と組み合わせて使用することを目的としたラップされた PST プロバイダーを実装しています。 サンプル ラップ PST ストア プロバイダーのダウンロードとインストールの詳細については、「サンプル ラップされた PST ストア プロバイダーのインストール [」を参照してください](installing-the-sample-wrapped-pst-store-provider.md)。 レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。
  
ラップされた PST ストア プロバイダーの使用が完了したら、ラップされた PST ストア プロバイダーを適切にシャットダウンする必要があります。 詳細については、「ラップされた PST ストア プロバイダー [をシャットダウンする」を参照してください](shutting-down-a-wrapped-pst-store-provider.md)。
  
## <a name="open-profile-section-routine"></a>Open Profile Section ルーチン

**[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** 関数は、現在のプロファイルのセクションを開きます。 この関数では、ラップされた PST ストア プロバイダーの実装で特別な処理が必要です。 要求された  `pgNSTGlobalProfileSectionGuid` 場合、関数はキャッシュされるプロファイル セクションを返します。 
  
### <a name="csupportopenprofilesection-example"></a>CSupport::OpenProfileSection() の例

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

- [ラップされた PST ストア プロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーのサンプルのインストール](installing-the-sample-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
- [ラップされた PST ストア プロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

