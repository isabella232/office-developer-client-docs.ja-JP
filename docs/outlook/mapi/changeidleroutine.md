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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1fbeccd805953322b579d1490b5e74e5132aa7ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19799809"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**適用されます**: Outlook 
  
[FNIDLE](fnidle.md)ベース アイドル ルーチンの特性の一部またはすべてを変更します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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

## <a name="parameters"></a>Parameters

_ftg_
  
> [in]アイドル ルーチンを識別するタグを機能します。 
    
_pfnIdle_
  
> [in]アイドル ルーチンへのポインター。 
    
_pvIdleParam_
  
> [in]新しいアイドル ルーチンの実装を呼び出し元が割り当てたメモリ ブロックへのポインター。 
    
_priIdle_
  
> [in]アイドル ルーチンの新しい優先度を表す値。 ルーチンの実装で定義可能な優先度よりも大きいか小さいは、0 が 0 ではありません。 0 の値は、マウスのクリックや、WM_PAINT メッセージなどのユーザー イベントに予約されています。 ゼロより大きい値は、ユーザー イベントよりも優先順位が高いと、Windows メッセージ ポンプの標準的なループの一部としてディスパッチをバック グラウンド タスクの優先順位を表します。 メッセージ ポンプのアイドル時間中にのみ実行しているアイドル状態のタスクの優先順位を表す 0 より小さい値です。 優先順位の例としては: 前景の提出書類の 1、1 電源編集文字の挿入、および新着メッセージをダウンロードするための 3。
    
_csecIdle_
  
> [in]時間を 100 分の 1 秒間、アイドル状態のルーチンに適用します。 初期時刻の値の意味は、 _iroIdle_パラメーターに渡される内容によって異なります。 できます。 
    
  - ユーザー何もしなかったため、MAPI の前に、までに必要な最小期間アイドル状態のエンジン ルーチンを呼び出すとアイドルを最初に、 _iroIdle_に FIROWAIT フラグが設定されている場合。 この時間が経過した後、アイドル状態のエンジンでは必要に応じてアイドル ルーチンを呼び出すことができます。 
    
  - _IroIdle_に FIROINTERVAL フラグが設定されている場合、アイドル状態のルーチンへの呼び出しの間の最小間隔。 
    
_iroIdle_
  
> [in]アイドル ルーチンを呼び出すための新しいオプションを示すフラグのビットマスクです。 次のフラグの 1 つだけを設定する必要があります。
    
  - FIROINTERVAL: _csecIdle_パラメーターによって指定される時間は、アイドル状態のルーチンへの連続呼び出しの間の最小の間隔です。 
      
  - FIROONCEONLY: 古い形式です。 使用しないでください。 
      
  - FIROPERBLOCK: 古い形式です。 使用しないでください。 
      
  - FIROWAIT: _csecIdle_パラメーターによって指定される時間は、ユーザー何もしなかったため、MAPI アイドル エンジンは、最初にアイドル ルーチンを呼び出す前に必要な経過時間の最小期間です。 この時間が経過した後、アイドル状態のエンジンでは必要に応じてアイドル ルーチンを呼び出すことができます。 
    
_ircIdle_
  
> [in]アイドル ルーチンに変更を示すために使用されるフラグのビットマスクです。 任意の組み合わせでは、次のフラグを設定できます。
    
  - FIRCCSEC: アイドル状態のルーチンでは、 _csecIdle_パラメーターで渡された値で示される変更に関連付けられている時間を変更します。 
      
  - FIRCIRO: アイドル状態のルーチンでは、オプションの変更は、値で示される変更パラメーターで渡された、 _iroIdle_です。 
      
  - FIRCPFN: アイドル状態の日常的なポインターの変更は、値で示される変更パラメーターで渡された、 _pfnIdle_です。 
      
  - FIRCPRI: アイドル状態のルーチンでは、優先順位の変更は、値で示される変更パラメーターで渡された、 _priIdle_です。 
      
  - FIRCPV: アイドル状態のルーチンでは、メモリ ブロックへの変更は、値で示される変更パラメーターで渡された、 _pvIdleParam_です。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。 
  
|**アイドル状態の日常的な関数**|**使用例**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |登録されているアイドル状態のルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録されているアイドル状態のルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
**ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。 
  
プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。 同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。 
  

