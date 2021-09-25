---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 43b5168f1d29ead887f884e6c61456c5ab28364b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575485"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>パラメーター

 _lpvReserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

**MAPIInitIdle 関数は**、初期化が成功した場合は 0 を返し、それ以外の場合は 1 を返します。 **MAPIInitIdle が** 複数回呼び出された場合、追加の呼び出しはすべて成功しますが、参照カウントを増やす以外は無視されます。 
  
## <a name="remarks"></a>注釈

クライアント アプリケーションまたはサービス プロバイダーは、他のアイドル 状態のエンジン関数を呼び出す前に **MAPIInitIdle** を呼び出す必要があります。 
  
**MAPIInitIdle** へのすべての呼び出しは [、MAPIDeInitIdle](mapideinitidle.md)への後続の呼び出しによって一致する必要があります。または、アイドル 状態のエンジンが呼び出し元のアプリケーションに対して実行された状態を残している必要があります。 
  
次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。 
  
|**アイドル ルーチン関数**|**使用状況**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録済みのアイドル ルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録済みのアイドル ルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。  <br/> |
|**MAPIInitIdle** <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。 同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。 
  

