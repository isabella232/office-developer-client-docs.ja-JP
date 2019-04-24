---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346656"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>パラメーター

 _lpvreserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

**MAPIInitIdle**関数は、初期化が成功した場合は0を返し、それ以外の場合は1を返します。 **MAPIInitIdle**が複数回呼び出された場合、追加の呼び出しはすべて成功しますが、参照カウントを増分する場合を除いて無視されます。 
  
## <a name="remarks"></a>解説

クライアントアプリケーションまたはサービスプロバイダーは、他の idle engine 関数を呼び出す前に、 **MAPIInitIdle**を呼び出す必要があります。 
  
**MAPIInitIdle**のすべての呼び出しは、以降の[MAPIDeInitIdle](mapideinitidle.md)の呼び出しで一致する必要があります。または、呼び出し元アプリケーションに対してアイドル状態のエンジンが実行されたままになります。 
  
次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。 
  
|**Idle ルーチン関数**|**使用法**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドルルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |登録されているアイドルルーチンを MAPI システムから削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |アイドルルーチンを MAPI システムに追加するか、有効にします。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。  <br/> |
|**MAPIInitIdle** <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。  <br/> |
   
プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。 同じ優先度のアイドルルーチン間での通話順序は保証されません。 
  

