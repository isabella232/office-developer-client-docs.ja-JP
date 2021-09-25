---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5721c4a99f6ead6fefa839b1c1e45fdd61d95c60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567782"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**適用対象**: Outlook 2013 | Outlook 2016 
  
[FNIDLE](fnidle.md)ベースのアイドル ルーチンの特性の一部またはすべてが変更されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a>パラメーター

_ftg_
  
> [in]アイドル ルーチンを識別する関数タグ。 
    
_pfnIdle_
  
> [in]アイドル 状態のルーチンへのポインター。 
    
_pvIdleParam_
  
> [in]呼び出し元の実装がアイドル ルーチンに割り当てる新しいメモリ ブロックへのポインター。 
    
_priIdle_
  
> [in]アイドル ルーチンの新しい優先度を表す値。 実装定義ルーチンで考えられる優先順位は、0 より大きいか、0 未満です。 値 0 は、マウスクリックやメッセージメッセージなどのユーザー イベントWM_PAINTされます。 0 より大きい値は、ユーザー イベントよりも優先度が高く、メッセージ ポンプ の標準ループの一部としてディスパッチされるバックグラウンド タスクWindows表します。 0 未満の値は、メッセージ ポンプアイドル時間中にのみ実行されるアイドル タスクの優先順位を表します。 優先順位の例としては、フォアグラウンド申請の場合は 1、電源編集文字の挿入には 1、新しいメッセージをダウンロードする場合は 3 です。
    
_csecIdle_
  
> [in]アイドル 状態のルーチンに適用する新しい時刻 (100 分の 1 秒)。 初期時間の値の意味は  _、iroIdle_ パラメーターで渡される内容に応じて異なります。 次の場合があります。 
    
  - FIROWAIT フラグが  _iroIdle_ に設定されている場合、MAPI アイドル エンジンがアイドル ルーチンを初めて呼び出す前に経過する必要があるユーザーの不作為の最小期間。 この時間が経過すると、アイドル エンジンは必要な頻度でアイドル ルーチンを呼び出す可能性があります。 
    
  - FIROINTERVAL フラグが  _iroIdle_ で設定されている場合、アイドル 状態のルーチンへの呼び出しの最小間隔。 
    
_iroIdle_
  
> [in]アイドル ルーチンを呼び出す新しいオプションを示すフラグのビットマスク。 次のいずれかのフラグを設定する必要があります。
    
  - FIROINTERVAL:  _csecIdle_ パラメーターで指定される時間は、アイドル ルーチンへの連続する呼び出しの最小間隔です。 
      
  - FIROONCEONLY: 廃止。 使用しないでください。 
      
  - FIROPERBLOCK: 廃止。 使用しないでください。 
      
  - FIROWAIT:  _csecIdle_ パラメーターで指定された時間は、MAPI アイドル エンジンがアイドル ルーチンを初めて呼び出す前に経過する必要があるユーザーの不作為の最小期間です。 この時間が経過すると、アイドル エンジンは必要な頻度でアイドル ルーチンを呼び出す可能性があります。 
    
_ircIdle_
  
> [in]アイドル ルーチンに加える変更を示すために使用されるフラグのビットマスク。 次のフラグは、任意の組み合わせで設定できます。
    
  - FIRCCSEC: アイドル ルーチンに関連付けられた時刻の変更、つまり  _、csecIdle_ パラメーターで渡された値によって示される変更。 
      
  - FIRCIRO: アイドル ルーチンのオプション (  _つまり、iroIdle_ パラメーターで渡された値によって示される変更) の変更。 
      
  - FIRCPFN: アイドル 状態のルーチン ポインター 、つまり  _pfnIdle_ パラメーターで渡された値によって示される変更を変更します。 
      
  - FIRCPRI: アイドル ルーチンの優先度に対する変更、つまり  _、priIdle_ パラメーターで渡された値によって示される変更。 
      
  - FIRCPV: アイドル ルーチンのメモリ ブロックへの変更、つまり  _、pvIdleParam_ パラメーターで渡された値によって示される変更。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。 
  
|**アイドル ルーチン関数**|**使用状況**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |登録済みのアイドル ルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録済みのアイドル ルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
**ChangeIdleRoutine** **、DeregisterIdleRoutine、****および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。 同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。 
  

