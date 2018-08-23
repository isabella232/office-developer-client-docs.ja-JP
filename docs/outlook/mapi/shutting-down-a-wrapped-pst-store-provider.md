---
title: ラップされた PST ストア プロバイダーのシャットダウン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0c9e5917-1b96-323d-bf8b-1d3aa1f677d0
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 5c8ad7443b0c1aa05f48284e4b09859ab53dd2c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803910"
---
# <a name="shutting-down-a-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーのシャットダウン

 
  
**適用対象**: Outlook 
  
ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーの使用が終了したら後、は、ラップされた PST ストア プロバイダーをシャット ダウンする必要があります正しく。 ラップされた PST ストア プロバイダーの使用に関する詳細については、「[ラップされた PST ストア プロバイダー](using-a-wrapped-pst-store-provider.md)」を参照してください。
  
ラップされた PST ストア プロバイダーを停止するには、 **[IMSProvider::Shutdown](imsprovider-shutdown.md)** 関数を呼び出す必要があります。 この関数は、正しい順序でラップされた PST ストア プロバイダーを閉じます。 
  
このトピックでは、 **IMSProvider::Shutdown**関数はサンプル ラップ PST ストア プロバイダーのコード例を使用して示されます。 レプリケーション API と連携して使用するものでは、ラップされた PST プロバイダーを実装します。 ダウンロードとサンプル ラップ PST ストア プロバイダーをインストールする方法の詳細については、「[サンプル ラップ PST ストア プロバイダーをインストールする](installing-the-sample-wrapped-pst-store-provider.md)」を参照してください。 レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。
  
## <a name="shut-down-routine"></a>シャット ダウン ルーチン

MAPI スプーラーは、ラップされた PST ストア プロバイダーが正常にシャット ダウンするようにラップされた PST ストア プロバイダーを解放する前に、 **[IMSProvider::Shutdown](imsprovider-shutdown.md)** 関数を呼び出します。 関数は、ラップされた PST ストア プロバイダーに関連付けられているすべてのセッション オブジェクトを終了します。 
  
## <a name="cmsprovidershutdown-example"></a>CMSProvider::ShutDown() の使用例

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

