---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410222"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[FNIDLE](fnidle.md)ベースのアイドルルーチンを有効または無効にします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>パラメーター

 _ftg_
  
> 順番有効または無効にする idle ルーチンを識別する関数タグ。 
    
 _fenable_
  
> 順番アイドルエンジンがアイドル状態のルーチンを有効にする必要がある場合は TRUE、無効にする場合は FALSE を指定します。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。 
  
|**Idle ルーチン関数**|**使用法**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドルルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |登録されているアイドルルーチンを MAPI システムから削除します。  <br/> |
|**EnableIdleRoutine** <br/> |登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |アイドルルーチンを MAPI システムに追加するか、有効にします。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。  <br/> |
   
 **changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。 同じ優先度のアイドルルーチン間での通話順序は保証されません。 
  

