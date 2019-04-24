---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334434"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**適用対象**: Outlook 2013 | Outlook 2016 
  
[FNIDLE](fnidle.md)ベースのアイドルルーチンの一部またはすべての特性を変更します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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
  
> 順番idle ルーチンを識別する Function タグ。 
    
_pfnidle_
  
> 順番アイドルルーチンへのポインター。 
    
_pvIdleParam_
  
> 順番呼び出し側の実装によってアイドルルーチンに対して割り当てられる新しいメモリブロックへのポインター。 
    
_アイドル状態_
  
> 順番アイドルルーチンの新しい優先度を表す値。 実装で定義されているルーチンの優先度は、0より大きい、または0より小さいです。 0の値は、マウスのクリックや WM_PAINT メッセージなどのユーザーイベントに対して予約されています。 0より大きい値は、ユーザーイベントより高い優先度を持つバックグラウンドタスクの優先度を表し、標準の Windows メッセージポンプループの一部としてディスパッチされます。 0未満の値は、メッセージポンプアイドル時間中にのみ実行されるアイドルタスクの優先度を表します。 優先度の例は、フォアグラウンド送信の場合は1、power edit 文字の挿入の場合は1、新しいメッセージをダウンロードする場合は3です。
    
_csecIdle_
  
> 順番アイドルルーチンに適用する新しい時間 (1/100 秒単位)。 最初の時刻の値の意味は、 _iroIdle_パラメーターで渡された内容によって異なります。 次のことが可能です。 
    
  - _iroIdle_で firowait フラグが設定されている場合に、MAPI idle engine が最初にアイドルルーチンを呼び出すまでに経過する必要がある、ユーザーの最小処理時間。 この時間が経過すると、アイドル状態のエンジンは、必要に応じて頻度の高いルーチンを呼び出すことができます。 
    
  - _iroIdle_で firointerval フラグが設定されている場合に、アイドルルーチンへの呼び出しの最小間隔。 
    
_iroIdle_
  
> 順番アイドルルーチンを呼び出すための新しいオプションを示すフラグのビットマスク。 次のフラグのいずれかを正確に設定する必要があります。
    
  - firointerval: _csecIdle_パラメーターで指定された時間は、アイドルルーチンへの連続する呼び出し間の最小間隔です。 
      
  - firoonly: Obsolete。 使用しないでください。 
      
  - FIROPERBLOCK: 廃止。 使用しないでください。 
      
  - firowait: _csecIdle_パラメーターで指定された時間は、MAPI アイドルエンジンが最初にアイドルルーチンを呼び出す前に経過する必要がある、ユーザーの最小処理時間です。 この時間が経過すると、アイドル状態のエンジンは、必要に応じて頻度の高いルーチンを呼び出すことができます。 
    
_ircidle_
  
> 順番アイドルルーチンに加えられる変更を示すために使用されるフラグのビットマスク。 次のフラグは、任意の組み合わせで設定できます。
    
  - [ファイヤ ccsec]: idle ルーチンに関連付けられている時間、つまり、 _csecIdle_パラメーターで渡された値によって示される変更点に対する変更。 
      
  - _iroIdle_パラメーターで渡された値によって示される変更である、アイドルルーチンのオプションに対する変更。 
      
  - [ファイヤ cpfn]: idle ルーチンポインターへの変更 (つまり、 _pfnidle_パラメーターに渡された値によって示される変更)。 
      
  - [ファイヤ cpri]: idle _idle_パラメーターで渡された値によって示される変更である、アイドルルーチンの優先度の変更。 
      
  - [ファイヤ cpv]: idle ルーチンのメモリブロックに対する変更 (つまり、 _pvIdleParam_パラメータで渡された値によって示される変更)。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。 
  
|**Idle ルーチン関数**|**使用法**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |登録されているアイドルルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |登録されているアイドルルーチンを MAPI システムから削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |アイドルルーチンを MAPI システムに追加するか、有効にします。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。  <br/> |
   
**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。 同じ優先度のアイドルルーチン間での通話順序は保証されません。 
  

