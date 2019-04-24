---
title: ラップされた PST ストアプロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: '最終更新日: 2012 年7月2日'
ms.openlocfilehash: fa918920213ee77c4d0c1d3ccc239ae7cffe81fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282783"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>ラップされた PST ストアプロバイダーのシャットダウン

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップされた個人用フォルダーファイル (pst) ストアプロバイダーの使用が終了したら、ラップされた PST ストアプロバイダーを適切にシャットダウンする必要があります。 ラップされた pst ストアプロバイダーの使用の詳細については、「ラップされ[た pst ストアプロバイダーの使用](using-a-wrapped-pst-store-provider.md)」を参照してください。
  
ラップされた PST ストアプロバイダーをシャットダウンするには、 **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** 関数を呼び出す必要があります。 この関数は、ラップされた PST ストアプロバイダーを正しい順序で閉じます。 
  
このトピックでは、サンプルのラップされた PST ストアプロバイダーのコード例を使用して、 **IMSProvider:: Shutdown**関数をデモンストレーションします。 このサンプルでは、レプリケーション API と共に使用することを目的とした、ラップされた PST プロバイダーを実装しています。 サンプルのラップされた pst ストアプロバイダーのダウンロードとインストールの詳細については、「[サンプルのラップされた pst ストアプロバイダーのインストール](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。 レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。
  
## <a name="shut-down-routine"></a>ルーチンをシャットダウンする

MAPI スプーラーは、ラップされた pst ストアプロバイダーを適切にシャットダウンできるように、ラップされた pst ストアプロバイダーを解放する直前に、 **[IMSProvider:: Shutdown](imsprovider-shutdown.md)** 関数を呼び出します。 この関数は、ラップされた PST ストアプロバイダーに関連付けられているすべてのセッションオブジェクトを終了します。 
  
## <a name="cmsprovidershutdown-example"></a>cmsprovider:: ShutDown () の例

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



[ラップされた PST ストアプロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
  
[ラップされた PST ストアプロバイダーのサンプルのインストール](installing-the-sample-wrapped-pst-store-provider.md)
  
[ラップされた PST ストアプロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストアプロバイダーの使用](using-a-wrapped-pst-store-provider.md)

