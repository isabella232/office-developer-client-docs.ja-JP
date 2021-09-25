---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: MAPI 初期化モニター
Last modified: April 27, 2021
ms.openlocfilehash: 13992b8094429b61e5f980653b621d0e188ce8c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588330"
---
# <a name="createmapiinitializationmonitor"></a>CreateMAPIInitializationMonitor

**適用対象 :** Outlook 2016 |Outlook 2019
  
## <a name="mapi-initialization-monitor"></a>MAPI 初期化モニター

MAPI を使用するアプリケーションが、初期化が完了した時間を知りたい場合があります。 たとえば、MAPI を初期化できる複数のスレッドがある場合や、アプリケーションの初期化中に MAPI が初期化された場合は、何らかの処理を実行する必要がありますが、MAPI スタックを常にスピンアップする必要はありません。 初期化モニターは、関数 (OLMAPI32.DLL からエクスポート) と、以下に示すいくつかの簡単なインターフェイスを使用して、この機能を提供します。

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```

#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)

OLMAPI32.DLL からエクスポートされたこのエントリ ポイントを使用すると、呼び出し元はインターフェイスを取得して、現在の初期化状態を照会したり、初期化完了用のコールバックをセットアップしたり、完了するまで現在のスレッドをブロックすることができます。 この API から返されるオブジェクトは再利用可能でスレッド セーフであり、それを取得したスレッドではなく、任意のスレッドから呼び出すことができます。 また、MAPI から公開される他のオブジェクトとは異なり、このオブジェクトは、DLL が読み込まれている限り有効であり、初期化セッション間で再使用できます。MAPIInitialize が呼び出される前または後に使用できます。 COM 標準 HRESULT を使用して成功または失敗を返し、IMAPIInitMonitor のインスタンスに out パラメーターを割り当てる。
  
## <a name="parameters"></a>パラメーター
  
 _ppInitMonitor_
> [out]MAPI 初期化モニターの新しく作成されたインスタンスを受信するポインター。
  
## <a name="return-values"></a>戻り値

S_OK
> 初期化モニターの新しいインスタンスが正常に作成されました。

E_OUTOFMEMORY
> 新しいオブジェクトをクレートするのに十分なメモリがなかった。

## <a name="see-also"></a>関連項目
[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
