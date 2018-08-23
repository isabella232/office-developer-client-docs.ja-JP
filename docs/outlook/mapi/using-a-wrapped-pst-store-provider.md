---
title: ラップされた PST ストア プロバイダーを使用します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: 4a2ccbbcdd3459af6b69156d80b37695251ba8d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804194"
---
# <a name="using-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーを使用します。

**適用対象**: Outlook 
  
ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーを使用することができます、前に初期化し、ラップされた PST ストア プロバイダーを構成する必要があります。 ラップされた PST ストア プロバイダーを構成した後、できるように、MAPI スプーラーと MAPI にログオンできます、メッセージ ストア プロバイダーの機能を実装しなければなりません。 初期化し、ラップされた PST ストア プロバイダーへのログインの詳細については、[ラップ PST ストア プロバイダーを初期化](initializing-a-wrapped-pst-store-provider.md)し、[ラップ PST ストア プロバイダーへのログ](logging-on-to-a-wrapped-pst-store-provider.md)を参照してください。
  
**[IMAPISupport::IUnknown](imapisupportiunknown.md)** インターフェイスは、プロバイダーを格納するメッセージでよく実行されるタスクの実装を提供します。 サンプル ラップ PST ストア プロバイダーの機能をこのインターフェイスをラップする必要があります。 **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** 関数には、特別な実装が必要です。 他のすべての関数は、ラップされたオブジェクトにパラメーターを渡すことができます。 
  
このトピックでは、 **IMAPISupport::OpenProfileSection**関数はサンプル ラップ PST ストア プロバイダーのコード例を使用して示されます。 レプリケーション API と連携して使用するものでは、ラップされた PST プロバイダーを実装します。 ダウンロードとサンプル ラップ PST ストア プロバイダーをインストールする方法の詳細については、「[サンプル ラップ PST ストア プロバイダーをインストールする](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。 レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。
  
ラップされた PST ストア プロバイダーを使用してが完了したらは、ラップされた PST ストア プロバイダーをシャット ダウンする必要があります正しく。 詳細については、[シャット ダウン、ラップされた PST ストア プロバイダー](shutting-down-a-wrapped-pst-store-provider.md)を参照してください。
  
## <a name="open-profile-section-routine"></a>プロファイル セクションの開いているルーチン

**[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** 関数は、現在のプロファイルのセクションを開きます。 関数は、ラップされた PST ストア プロバイダーの実装で特別な処理を必要とします。 `pgNSTGlobalProfileSectionGuid`が要求されると、キャッシュされているプロファイルのセクションを返します。 
  
### <a name="csupportopenprofilesection-example"></a>CSupport::OpenProfileSection() の使用例

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

