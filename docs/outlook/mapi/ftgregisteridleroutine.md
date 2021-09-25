---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0ba14e2cb0b7c41460a54f31e80099ddfb27cfb7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621025"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI システム [に FNIDLE](fnidle.md) 関数ベースのアイドル ルーチンを追加します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a>パラメーター

_pfnIdle_
  
> [in]アイドル 状態のルーチンへのポインター。 
    
_pvIdleParam_
  
> [in]アイドル エンジンが呼び出し時に、アイドル 状態のルーチンにパラメーターとして渡す必要があるメモリ ブロックへのポインター。 
    
_priIdle_
  
> [in]アイドル 状態のルーチンの最初の優先度。 実装定義ルーチンで考えられる優先順位は、0 より大きいか、0 未満です。 0 の優先度は、マウスクリックやメッセージメッセージなどのユーザー イベントWM_PAINTされます。 優先度が 0 より大きい場合は、ユーザー イベントよりも優先度が高く、メッセージ ポンプ の標準ループの一部Windowsバックグラウンド タスクを表します。 優先度が 0 未満の場合は、メッセージ ポンプのアイドル時間中にのみ実行されるアイドル タスクを表します。 優先順位の例は、フォアグラウンド申請の場合は 1、電源編集文字の挿入には 2、新しいメッセージをダウンロードする場合は 3 です。
    
_csecIdle_
  
> [in]アイドル 状態のルーチン パラメーターを指定する場合に使用する初期時間値 (100 分の 1 秒)。 初期時間の値の意味は  _、iroIdle_ パラメーターで渡される内容に応じて異なります。 意味は、次のいずれかを指定できます。 
    
  - FIROWAIT フラグが  _iroIdle_ に設定されている場合、MAPI アイドル エンジンがアイドル ルーチンを初めて呼び出す前に経過する必要があるユーザーの不作為の最小期間。 この時間が経過すると、アイドル エンジンは必要な頻度でアイドル ルーチンを呼び出す可能性があります。 
    
  - FIROINTERVAL フラグが  _iroIdle_ で設定されている場合、アイドル 状態のルーチンへの呼び出しの最小間隔。 
    
_iroIdle_
  
> [in]アイドル ルーチンの初期オプションを設定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
  FIRONOADJUSTMENT
    
  > このフラグを使用して、アイドル 状態のルーチン タイマーをスリープまたは再開に合わせて調整しなけれと指定します。 このフラグのない既定の動作は、経過時間の計算時にスリープ時間が除外されます。 FIRONOADJUSTMENT が渡された場合、経過時間の計算時にスリープ時間が含まれます。
      
  FIRODISABLED
    
  > 登録時にアイドル ルーチンを無効にする必要があります。 既定のアクションは **、FtgRegisterIdleRoutine** が登録するときにアイドル ルーチンを有効にします。 
      
  FIROINTERVAL 
    
  > _csecIdle_ パラメーターで指定される時間は、アイドル ルーチンへの連続する呼び出しの最小間隔です。 
      
  FIROONCEONLY 
    
  > 現在使用されていません。使用しないでください。  
      
  FIROPERBLOCK 
    
  > 現在使用されていません。使用しないでください。  
      
  FIROWAIT 
    
  > _csecIdle_ パラメーターで指定される時間は、MAPI アイドル エンジンがアイドル ルーチンを初めて呼び出す前に経過する必要があるユーザーの不作為の最小期間です。 この時間が経過すると、アイドル エンジンは必要な頻度でアイドル ルーチンを呼び出す可能性があります。 
    
## <a name="return-value"></a>戻り値

**FtgRegisterIdleRoutine** 関数は、MAPI システムに追加されたアイドル ルーチンを識別する関数タグを返します。 **FtgRegisterIdleRoutine** が、メモリの問題などのためにクライアント アプリケーションまたはサービス プロバイダーのアイドル ルーチンを登録できない場合は、NULL を返します。 
  
## <a name="remarks"></a>注釈

次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。 
  
|**アイドル ルーチン関数**|**使用状況**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録済みのアイドル ルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録済みのアイドル ルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。  <br/> |
|**FtgRegisterIdleRoutine** <br/> |MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
**ChangeIdleRoutine** **、DeregisterIdleRoutine、****および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。 同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。 
  
iroIdle パラメーターで FIRONOADJUSTMENT フラグを使用する例  _を次に示_ します。 
  
1. 5 分の遅延でアイドル 状態のルーチンを登録します。
    
2. 休止状態/1 分後にコンピューターをスリープ状態 (タイマーの残り 4 分)。
    
3. 10 分後にコンピューターを再開します。
    
FIRONOADJUSTMENT を使用しない既定の動作は、ルーチンが実行するまでにさらに 4 分待機する必要があるという点です。 つまり、タイマーが調整され、コンピューターがスリープ状態にされた時間を指定できます。 ただし、FIRONOADJUSTMENT に合格すると、5 分以上のリアルタイムが経過したため、アイドル ルーチンはすぐに実行されます。
  

