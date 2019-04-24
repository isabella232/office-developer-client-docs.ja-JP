---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327994"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**適用対象**: Outlook 2013 | Outlook 2016 
  
[FNIDLE](fnidle.md)関数ベースのアイドルルーチンを MAPI システムに追加します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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

_pfnidle_
  
> 順番アイドルルーチンへのポインター。 
    
_pvIdleParam_
  
> 順番アイドル状態のエンジンが、その呼び出し時にアイドルルーチンにパラメーターとして渡す必要があるメモリブロックへのポインター。 
    
_アイドル状態_
  
> 順番アイドルルーチンの初期優先度。 実装で定義されているルーチンの優先度は、0より大きい、または0より小さいです。 優先度0は、マウスクリックや WM_PAINT メッセージなどのユーザーイベント用に予約されています。 0より大きい優先度は、ユーザーイベントより高い優先度を持つバックグラウンドタスクを表し、標準の Windows メッセージポンプループの一部としてディスパッチされます。 0未満の優先度は、メッセージポンプのアイドル時間にのみ実行されるアイドルタスクを表します。 優先度の例は、フォアグラウンド送信の場合は1、power edit 文字の挿入の場合は2、新しいメッセージをダウンロードする場合は3です。
    
_csecIdle_
  
> 順番アイドルルーチンパラメーターの指定に使用される初期時間値 (1/100 秒単位)。 最初の時刻の値の意味は、 _iroIdle_パラメーターで渡された内容によって異なります。 この意味には、次のいずれかを指定できます。 
    
  - _iroIdle_で firowait フラグが設定されている場合に、MAPI idle engine が最初にアイドルルーチンを呼び出すまでに経過する必要がある、ユーザーの最小処理時間。 この時間が経過すると、アイドル状態のエンジンは、必要に応じて頻度の高いルーチンを呼び出すことができます。 
    
  - _iroIdle_で firointerval フラグが設定されている場合に、アイドルルーチンへの呼び出しの最小間隔。 
    
_iroIdle_
  
> 順番アイドルルーチンの初期オプションを設定するために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
  FIRONOADJUSTMENT
    
  > このフラグを使用して、アイドルルーチンタイマーをスリープまたは再開に調整しないように指定します。 このフラグを使用しない既定の動作では、経過時間の計算時にスリープ時間が除外されます。 FIRONOADJUSTMENT が渡された場合、経過時間を計算するときにスリープ時間が含まれます。
      
  firodisabled
    
  > 登録時にアイドルルーチンを無効にする必要があります。 既定のアクションは、 **FtgRegisterIdleRoutine**が登録時に idle ルーチンを有効にすることです。 
      
  firointerval 
    
  > _csecIdle_パラメーターによって指定された時間は、アイドルルーチンへの連続する呼び出し間の最小間隔です。 
      
  firoonly のみ 
    
  > 使用されていません。 使用しないでください。 
      
  FIROPERBLOCK 
    
  > 使用されていません。 使用しないでください。 
      
  firowait 
    
  > _csecIdle_パラメーターによって指定された時間は、ユーザーが最初にアイドル状態のルーチンを呼び出すまでに経過する必要がある、ユーザーの最小処理時間です。 この時間が経過すると、アイドル状態のエンジンは、必要に応じて頻度の高いルーチンを呼び出すことができます。 
    
## <a name="return-value"></a>戻り値

**FtgRegisterIdleRoutine**関数は、MAPI システムに追加された idle ルーチンを識別する関数タグを返します。 **FtgRegisterIdleRoutine**が、メモリの問題などのために、クライアントアプリケーションまたはサービスプロバイダーの idle ルーチンを登録できない場合は、NULL を返します。 
  
## <a name="remarks"></a>解説

次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドル状態のルーチンを処理します。 
  
|**Idle ルーチン関数**|**使用法**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドルルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |登録されているアイドルルーチンを MAPI システムから削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。  <br/> |
|**FtgRegisterIdleRoutine** <br/> |アイドルルーチンを MAPI システムに追加するか、有効にします。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。  <br/> |
   
**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。 同じ優先度のアイドルルーチン間での通話順序は保証されません。 
  
_iroIdle_パラメーターで FIRONOADJUSTMENT フラグを使用する例を次に示します。 
  
1. アイドルルーチンに5分の遅延を登録します。
    
2. 休止/コンピューターを1分後 (タイマーの左から4分) にします。
    
3. コンピューターを10分後に再開します。
    
FIRONOADJUSTMENT を使用しない既定の動作では、ルーチンが実行されるまでに4分間待機する必要があります。 つまり、タイマーは、コンピューターがスリープ状態になっていた時間を確保するように調整されています。 ただし、FIRONOADJUSTMENT を渡した場合、アイドルルーチンは、リアルタイムが5分以上経過したため、直ちに実行されます。
  

