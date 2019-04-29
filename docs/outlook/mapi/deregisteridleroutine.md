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
  
MAPI システムから[FNIDLE](fnidle.md)ベースのアイドルルーチンを削除します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>パラメーター

 _ftg_
  
> 順番削除する idle ルーチンを識別する Function タグです。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

クライアントアプリケーションまたはサービスプロバイダーのすべてのタスクは、有効な_ftg_パラメーターを持つ idle ルーチンを登録解除できます。 特に、アイドル状態のルーチンで自分自身を登録解除することができます。 
  
次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。 
  
|**Idle ルーチン関数**|**使用法**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドルルーチンの特性を変更します。  <br/> |
|**DeregisterIdleRoutine** <br/> |登録されているアイドルルーチンを MAPI システムから削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |アイドルルーチンを MAPI システムに追加するか、有効にします。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。  <br/> |
   
 **changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。 同じ優先度のアイドルルーチン間での通話順序は保証されません。 
  
アイドル状態のルーチンが登録解除された後は、アイドル状態のエンジンはそれを再度呼び出しません。 **DeregisterIdleRoutine**を呼び出す実装では、 **FtgRegisterIdleRoutine**関数への元の呼び出しで使用するために、アイドルエンジンがポインターを渡したメモリブロックを解放する必要があります。 
  

