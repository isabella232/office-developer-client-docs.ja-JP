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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404562"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI システムから [FNIDLE ベース](fnidle.md) のアイドル ルーチンを削除します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>パラメーター

 _ftg_
  
> [in]削除するアイドル ルーチンを識別する関数タグ。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

クライアント アプリケーションまたはサービス プロバイダー内のタスクは、有効な ftg パラメーターを持つアイドル ルーチンを  _登録解除_ できます。 特に、アイドル 状態のルーチンは、それ自体を登録解除できます。 
  
次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。 
  
|**アイドル ルーチン関数**|**使用状況**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録済みのアイドル ルーチンの特性を変更します。  <br/> |
|**DeregisterIdleRoutine** <br/> |MAPI システムから登録済みのアイドル ルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
 **ChangeIdleRoutine** **、DeregisterIdleRoutine、****および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。 同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。 
  
アイドル ルーチンの登録が解除された後、アイドル 状態のエンジンは再び呼び出しません。 **DeregisterIdleRoutine** を呼び出す実装では、アイドル エンジンが **FtgRegisterIdleRoutine** 関数への元の呼び出しで使用するポインターを渡したメモリ ブロックを割り当て解除する必要があります。 
  

