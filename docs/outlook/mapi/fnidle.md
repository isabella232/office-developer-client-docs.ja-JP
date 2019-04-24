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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342246"
---
# <a name="fnidle"></a>FNIDLE
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI アイドルエンジンが優先度に従って定期的に呼び出すアイドルルーチンを定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|定義された関数の実装:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI  <br/> |
|対応するポインターの種類:  <br/> |pfnidle  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>パラメーター

 _lpvcontext_
  
> 順番MAPI が呼び出しを行うたびにアイドルルーチンに渡されるメモリブロックへのポインター。 このポインターは、 [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)によって_pvIdleParam_パラメーターの MAPI アイドルエンジンに渡されます。 メモリブロック内のデータは、操作対象のオブジェクトや、時間のかかる操作の現在の状態など、アイドルルーチンの呼び出しのコンテキストを提供できます。
    
## <a name="return-value"></a>戻り値

FALSE 
  
> **FNIDLE**プロトタイプが指定されたアイドルルーチンは、常に FALSE を返します。 
    
## <a name="remarks"></a>解説

アイドルルーチンの特定の機能は、クライアントアプリケーションまたはサービスプロバイダーを実装することによって決まります。 
  
クライアントまたはプロバイダーは、アイドルルーチンの各状態の実行時間を制限する必要があります。 すべての状態は、最小限の処理を実行し、 _lpvcontext_が指すコンテキストデータ内の現在の状態を更新して、MAPI アイドルエンジンに戻る必要があります。 
  
クライアントまたはプロバイダーは、 [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)関数への呼び出しを使用して独自のアイドルルーチンを登録する前に、MAPI 関数[MAPIInitIdle](mapiinitidle.md)を呼び出す必要があります。 
  
次の関数は、MAPI アイドルエンジンと、FNIDLE 関数プロトタイプに基づいてアイドルルーチンを処理します。 
  
|**Idle ルーチン関数**|**使用法**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドルルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |登録されているアイドルルーチンを MAPI システムから削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |アイドルルーチンを MAPI システムに追加するか、有効にします。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。  <br/> |
   
**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。 同じ優先度のアイドルルーチン間での通話順序は保証されません。 
  

