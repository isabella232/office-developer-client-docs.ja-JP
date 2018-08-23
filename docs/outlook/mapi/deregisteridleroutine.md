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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 78d499dabe60a8051c6a2a77abad4b7d6f2ed159
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591955"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

## <a name="parameters"></a>パラメーター

 _ftg_
  
> [in]関数を削除するのにはアイドル状態のルーチンを識別するタグです。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

_Ftg_の有効なパラメーターを持っている、アイドル状態のルーチンはクライアント アプリケーションまたはサービス プロバイダーの任意のタスクの登録を解除できます。 具体的には、アイドル、ルーチンが登録を解除自体。 
  
次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。 
  
|**アイドル状態の日常的な関数**|**使用状況**|
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
  

