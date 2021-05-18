---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408209"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a>パラメーター

なし。 
  
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

クライアント アプリケーションまたはサービス プロバイダーは、アイドル 状態のエンジンが不要になったときに **MAPIDeInitIdle** を呼び出す必要があります 。たとえば、処理を停止する場合などです。 
  
[MAPIInitIdle](mapiinitidle.md)へのすべての呼び出しは **、MAPIDeInitIdle** への後続の呼び出しによって一致する必要があります。または、アイドル 状態のエンジンが呼び出し元のアプリケーションに対して実行された状態を残している必要があります。 
  
次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。 
  
|**アイドル ルーチン関数**|**使用状況**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録済みのアイドル ルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録済みのアイドル ルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。  <br/> |
|**MAPIDeInitIdle** <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。 同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。 
  

