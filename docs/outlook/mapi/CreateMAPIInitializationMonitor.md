---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: MAPI 初期化モニター
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062054"
---
# <a name="createmapiinitializationmonitor"></a>CreateMAPIInitializationMonitor

**適用対象 :** Outlook 2016 |Outlook 2019
  
## <a name="mapi-initialization-monitor"></a>MAPI 初期化モニター

MAPI を使用するアプリケーションが、初期化が完了した時間を知りたい場合があります。 たとえば、MAPI を初期化できる複数のスレッドがある場合や、アプリケーションの初期化中に MAPI が初期化された場合は、何らかの処理を実行する必要がありますが、MAPI スタックを常にスピンアップする必要はありません。 初期化モニターは、関数 (OLMAPI32.DLL からエクスポート) と、以下に示すいくつかの簡単なインターフェイスを使用して、この機能を提供します。

これは、OLMAPI32.DLL からエクスポートされたエントリ ポイントです。これにより、呼び出し元はインターフェイスを取得して現在の初期化状態を照会したり、初期化完了用のコールバックをセットアップしたり、完了するまで現在のスレッドをブロックすることができます。 この API から返されるオブジェクトは再利用可能でスレッド セーフであり、それを取得したスレッドではなく、任意のスレッドから呼び出すことができます。 また、MAPI から公開される他のオブジェクトとは異なり、このオブジェクトは、DLL が読み込まれている限り有効であり、初期化セッション間で再使用できます。MAPIInitialize が呼び出される前または後に使用できます。 COM 標準 HRESULT を使用して成功または失敗を返し、IMAPIInitMonitor のインスタンスに out パラメーターを割り当てる。

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)

OLMAPI32.DLL からエクスポートされたこのエントリ ポイントを使用すると、呼び出し元はインターフェイスを取得して、現在の初期化状態を照会したり、初期化完了用のコールバックをセットアップしたり、完了するまで現在のスレッドをブロックすることができます。 この API から返されるオブジェクトは再利用可能でスレッド セーフであり、それを取得したスレッドではなく、任意のスレッドから呼び出すことができます。 また、MAPI から公開される他のオブジェクトとは異なり、このオブジェクトは、DLL が読み込まれている限り有効であり、初期化セッション間で再使用できます。MAPIInitialize が呼び出される前または後に使用できます。 COM 標準 HRESULT を使用して成功または失敗を返し、IMAPIInitMonitor のインスタンスに out パラメーターを割り当てる。
  
## <a name="quick-info"></a>クイック ヒント

| 識別子 | result |
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |olmapi32.dll  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Outlook  <br/> |

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
