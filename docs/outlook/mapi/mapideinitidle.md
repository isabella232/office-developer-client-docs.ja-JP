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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4eaeb3338c95196ff346c5098e5d06371b00bc5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801491"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**適用されます**: Outlook 
  
呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a>Parameters

なし。 
  
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

クライアント アプリケーションまたはサービス プロバイダーは、不要になったときに必要なアイドル状態のエンジンでは、たとえば、処理を停止しようとしているときに**MAPIDeInitIdle**を呼び出す必要があります。 
  
[MAPIInitIdle](mapiinitidle.md)へのすべての呼び出しを**MAPIDeInitIdle**、それ以降の呼び出しに一致する必要があるまたは呼び出し元のアプリケーションを実行しているアイドル状態のエンジンのままです。 
  
次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。 
  
|**アイドル状態の日常的な関数**|**使用例**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |登録されているアイドル状態のルーチンの特性を変更します。  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |MAPI システムから登録されているアイドル状態のルーチンを削除します。  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。  <br/> |
|**MAPIDeInitIdle** <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。  <br/> |
   
プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。 同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。 
  

