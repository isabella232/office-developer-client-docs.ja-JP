---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bf1a84a1f305580fc9d9085753ab7eb5c62b8aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800093"
---
# <a name="fnidle"></a>FNIDLE
 
**適用されます**: Outlook 
  
MAPI アイドル エンジンを呼び出すの優先順位に従って定期的にアイドル状態のルーチンを定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装される関数の定義:  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI  <br/> |
|対応するポインターの型。  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameters

 _lpvContext_
  
> [in]アイドル ルーチンへの MAPI のパスは時間、メモリ ブロックへのポインターは、それを呼び出します。 このポインターは、 [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)で、 _pvIdleParam_パラメーターでは、MAPI アイドル エンジンに渡されます。 メモリ ブロック内のデータは、操作対象のオブジェクトなど、アイドル状態のルーチンまたは時間のかかる操作の現在の状態への呼び出しのコンテキストを提供できます。
    
## <a name="return-value"></a>�߂�l

FALSE 
  
> **FNIDLE**プロトタイプでアイドル状態のルーチンは、FALSE を返す常にする必要があります。 
    
## <a name="remarks"></a>備考

アイドル ルーチンの特定の機能は、実装することによって決定されますクライアント アプリケーションまたはサービス プロバイダーです。 
  
クライアントまたはプロバイダーは、実行時間、アイドル状態のルーチンの各状態を制限する必要があります。 すべての状態では、最小限の処理を実行、 _lpvContext_で示されるコンテキスト データの現在の状態を更新、および MAPI アイドル エンジンに戻る必要があります。 
  
クライアントまたはプロバイダーは、 [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)関数を呼び出して、独自のアイドル状態のルーチンを登録する前に MAPI 関数[MAPIInitIdle](mapiinitidle.md)を呼び出す必要があります。 
  
次の関数では、MAPI アイドル エンジンと FNIDLE 関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。 
  
|**アイドル状態の日常的な関数**|**使用例**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドル状態のルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録されているアイドル状態のルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
**ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。 
  
プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。 同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。 
  

