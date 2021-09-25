---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c8bc1a38693f0bfc83d5d17cca1a1bb38f971de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556085"
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
  

