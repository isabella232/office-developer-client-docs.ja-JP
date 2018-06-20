---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 85161fb87e798bbb03b267f9760870da1246e48d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799909"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**適用されます**: Outlook 
  
MAPI システムからのアイドル状態のルーチンを削除する[FNIDLE](fnidle.md)に基づいています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Parameters

 _ftg_
  
> [in]関数を削除するのにはアイドル状態のルーチンを識別するタグです。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

_Ftg_の有効なパラメーターを持っている、アイドル状態のルーチンはクライアント アプリケーションまたはサービス プロバイダーの任意のタスクの登録を解除できます。 具体的には、アイドル、ルーチンが登録を解除自体。 
  
次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。 
  
|**アイドル状態の日常的な関数**|**使用例**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドル状態のルーチンの特性を変更します。  <br/> |
|**DeregisterIdleRoutine** <br/> |MAPI システムから登録されているアイドル状態のルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
 **ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。 
  
プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。 同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。 
  
アイドル ルーチンの登録を解除した後、アイドル状態のエンジンが呼び出されません、もう一度。 **DeregisterIdleRoutine**を呼び出す任意の実装は、 **FtgRegisterIdleRoutine**関数の元の呼び出しで使用するアイドル状態のエンジンのポインターを渡すようにすべてのメモリ ブロックを解放する必要があります。 
  

