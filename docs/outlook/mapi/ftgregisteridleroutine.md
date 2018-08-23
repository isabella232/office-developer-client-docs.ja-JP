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
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800139"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**適用対象**: Outlook 
  
MAPI システムには、 [FNIDLE](fnidle.md)関数に基づくアイドル ルーチンを追加します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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
  
> [in]アイドル ルーチンへのポインター。 
    
_pvIdleParam_
  
> [in]アイドル状態のエンジンは、アイドル ルーチンにそれを呼び出すときで、パラメーターとして渡す必要があるメモリ ブロックへのポインター。 
    
_priIdle_
  
> [in]アイドル ルーチンの最初の優先順位です。 ルーチンの実装で定義可能な優先度よりも大きいか小さいは、0 が 0 ではありません。 0 の優先順位は、マウスのクリックや、WM_PAINT メッセージなどのユーザー イベントに予約されています。 優先度が 0 より大きい値は、ユーザー イベントよりも優先順位が高いと、Windows メッセージ ポンプの標準的なループの一部としてディスパッチをバック グラウンド タスクを表します。 0 より小さい値の優先順位は、メッセージ ポンプのアイドル時間中にのみ実行しているアイドル状態のタスクを表します。 優先順位の例としては次のとおり: フォア グラウンドの提出書類の 1、2 電源編集文字の挿入、および 3 の新しいメッセージをダウンロードするためです。
    
_csecIdle_
  
> [in]初期の時間の値を 100 分の 1 秒間、アイドル状態の日常的なパラメーターを指定するときに使用します。 初期時刻の値の意味は、 _iroIdle_パラメーターに渡される内容によって異なります。 意味には、次のいずれかを指定できます。 
    
  - ユーザー何もしなかったため、MAPI の前に、までに必要な最小期間アイドル状態のエンジン ルーチンを呼び出すとアイドルを最初に、 _iroIdle_に FIROWAIT フラグが設定されている場合。 この時間が経過した後、アイドル状態のエンジンでは必要に応じてアイドル ルーチンを呼び出すことができます。 
    
  - _IroIdle_に FIROINTERVAL フラグが設定されている場合、アイドル状態のルーチンへの呼び出しの間の最小間隔。 
    
_iroIdle_
  
> [in]アイドル ルーチンの最初のオプションを設定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
  FIRONOADJUSTMENT
    
  > スリープのアイドル状態の定期的なタイマーを調整しないことを指定するのにはこのフラグを使用して停止または再開します。 このフラグを設定しないデフォルトの動作では、経過時間を計算するときに、スリープ時間を除外します。 FIRONOADJUSTMENT が渡された場合、スリープ時間は含まれている経過時間を計算する場合です。
      
  FIRODISABLED
    
  > 登録されている場合は、アイドル状態のルーチンを無効にする必要があります。 既定のアクションは、 **FtgRegisterIdleRoutine**がそれを登録すると、アイドル状態のルーチンを有効にするのには。 
      
  FIROINTERVAL 
    
  > _CsecIdle_パラメーターによって指定される時間は、アイドル状態のルーチンへの連続呼び出しの間の最小の間隔です。 
      
  FIROONCEONLY 
    
  > 現在使用されていません。使用しないでください。  
      
  FIROPERBLOCK 
    
  > 現在使用されていません。使用しないでください。  
      
  FIROWAIT 
    
  > _CsecIdle_パラメーターによって指定される時間は、ユーザー何もしなかったため、MAPI アイドル エンジンは、最初にアイドル ルーチンを呼び出す前に必要な経過時間の最小期間です。 この時間が経過した後、アイドル状態のエンジンでは必要に応じてアイドル ルーチンを呼び出すことができます。 
    
## <a name="return-value"></a>戻り値

**FtgRegisterIdleRoutine**関数では、MAPI システムに追加されたアイドル ルーチンを識別する関数のタグを取得します。 **FtgRegisterIdleRoutine**は、クライアント アプリケーションまたはサービス プロバイダーのアイドル状態のルーチンを登録できません、する場合は、メモリの問題のため NULL を返します。 
  
## <a name="remarks"></a>注釈

次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを扱います。 
  
|**アイドル状態の日常的な関数**|**使用状況**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドル状態のルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録されているアイドル状態のルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。  <br/> |
|**FtgRegisterIdleRoutine** <br/> |MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
**ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。 
  
プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。 同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。 
  
次は、 _iroIdle_パラメーターに FIRONOADJUSTMENT フラグを使用する場合の例です。 
  
1. 5 分遅れで、アイドル状態のルーチンを登録します。
    
2. 休止状態やスリープ、コンピューター後 1 分 (4 分のタイマーのまま)。
    
3. 10 分後、コンピューターを再開します。
    
FIRONOADJUSTMENT、せず、既定の動作では、4 分のルーチンを実行するを待機する必要がまだします。 タイマーは、コンピューターがスリープする時間をできるように調整されました。 ただし、FIRONOADJUSTMENT に合格した場合、アイドル ルーチンが実行直後にリアルタイムの 5 分以上が経過したためです。
  

