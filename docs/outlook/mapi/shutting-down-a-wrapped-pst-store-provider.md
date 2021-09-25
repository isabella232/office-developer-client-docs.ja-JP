---
title: ラップされた PST ストア プロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 3f4aa55a8b557c8c14678bea618b761a22d7f96a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619758"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーのシャットダウン

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップされた個人用フォルダー ファイル (PST) ストア プロバイダーの使用が完了したら、ラップされた PST ストア プロバイダーを適切にシャットダウンする必要があります。 ラップされた PST ストア プロバイダーの使用の詳細については、「Wrapped PST ストア プロバイダーの使用 [」を参照してください](using-a-wrapped-pst-store-provider.md)。
  
ラップされた PST ストア プロバイダーをシャットダウンするには **[、IMSProvider::Shutdown 関数を呼び出す必要](imsprovider-shutdown.md)** があります。 この関数は、ラップされた PST ストア プロバイダーを順番に閉じます。 
  
このトピックでは、サンプル ラップされた PST ストア プロバイダーのコード例を使用して **、IMSProvider::Shutdown** 関数を示します。 このサンプルでは、レプリケーション API と組み合わせて使用することを目的としたラップされた PST プロバイダーを実装しています。 サンプル ラップ PST ストア プロバイダーのダウンロードとインストールの詳細については、「サンプル ラップされた PST ストア プロバイダーのインストール [」を参照してください](installing-the-sample-wrapped-pst-store-provider.md)。 レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。
  
## <a name="shut-down-routine"></a>シャットダウン ルーチン

MAPI スプーラーは、ラップされた PST ストア プロバイダーが適切にシャットダウンできるよう、ラップされた PST ストア プロバイダーを解放する直前に **[IMSProvider::Shutdown](imsprovider-shutdown.md)** 関数を呼び出します。 この関数は、ラップされた PST ストア プロバイダーに関連付けられているすべてのセッション オブジェクトを終了します。 
  
## <a name="cmsprovidershutdown-example"></a>CMSProvider::ShutDown() の例

```cpp
STDMETHODIMP CMSProvider::Shutdown(ULONG * pulFlags) 
{ 
    HRESULT hRes = S_OK; 
    Log(true,"CMSProvider::Shutdown\n"); 
    hRes =m_pPSTMS->Shutdown(pulFlags); 
    Log(true,"CMSProvider::Shutdown returned: 0x%08X\n", hRes); 
    return hRes ;  
}
```

## <a name="see-also"></a>関連項目



[ラップされた PST ストア プロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーのサンプルのインストール](installing-the-sample-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーの使用](using-a-wrapped-pst-store-provider.md)

