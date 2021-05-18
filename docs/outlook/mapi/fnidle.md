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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412381"
---
# <a name="fnidle"></a>FNIDLE
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI アイドル エンジンが優先度に応じて定期的に呼び出すアイドル ルーチンを定義します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI  <br/> |
|対応するポインターの種類:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>パラメーター

 _lpvContext_
  
> [in]MAPI が呼び出すごとにアイドル ルーチンに渡すメモリ ブロックへのポインター。 このポインターは [、FtgRegisterIdleRoutine](ftgregisteridleroutine.md)_によって pvIdleParam_ パラメーターの MAPI アイドル エンジンに渡されます。 メモリ ブロック内のデータは、どのオブジェクトを操作するか、長い操作の現在の状態など、アイドル 状態ルーチンへの呼び出しのコンテキストを提供できます。
    
## <a name="return-value"></a>戻り値

FALSE 
  
> FNIDLE プロトタイプを持つアイドル **状態のルーチン** は、常に FALSE を返す必要があります。 
    
## <a name="remarks"></a>注釈

アイドル ルーチンの特定の機能は、実装しているクライアント アプリケーションまたはサービス プロバイダーによって決まります。 
  
クライアントまたはプロバイダーは、アイドル 状態の各状態の実行時間を制限する必要があります。 すべての状態は、最小限の処理を実行し  _、lpvContext_ が指すコンテキスト データの現在の状態を更新し、MAPI アイドル エンジンに戻る必要があります。 
  
クライアントまたはプロバイダーは、独自のアイドル ルーチンを[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)関数への呼び出しで登録する前に、MAPI 関数[MAPIInitIdle](mapiinitidle.md)を呼び出す必要があります。 
  
次の関数は、MAPI アイドル エンジンと、FNIDLE 関数プロトタイプに基づくアイドル ルーチンを処理します。 
  
|**アイドル ルーチン関数**|**使用状況**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録済みのアイドル ルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録済みのアイドル ルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
**ChangeIdleRoutine** **、DeregisterIdleRoutine、****および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。 
  
プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。 同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。 
  

