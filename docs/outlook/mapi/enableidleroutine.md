---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d81fec5072b51c26291b16253d0fefa5bfa89f91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567684"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
FNIDLE ベースのアイドル [ルーチンを有効](fnidle.md) または無効にします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>パラメーター

 _ftg_
  
> [in]有効または無効にするアイドル ルーチンを識別する関数タグ。 
    
 _fEnable_
  
> [in]アイドル 状態のエンジンでアイドル ルーチンを有効にする必要がある場合は TRUE、無効にする必要がある場合は FALSE を含む。
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。 
  
|**アイドル ルーチン関数**|**使用状況**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録済みのアイドル ルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録済みのアイドル ルーチンを削除します。  <br/> |
|**EnableIdleRoutine** <br/> |MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
 **ChangeIdleRoutine** **、DeregisterIdleRoutine、****および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。 同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。 
  

