---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799790"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**適用対象**: Outlook 
  
メッセージ セッションおよびそのセッション内で作成されたすべてのメッセージを閉じます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>パラメーター

 _lpMsgSess_
  
> [in]メッセージ セッションの開始時に[OpenIMsgSession](openimsgsession.md)関数を使用して取得したメッセージのセッション オブジェクトへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

メッセージ セッションは、クライアント アプリケーションと基になる OLE **IStorage**オブジェクトの上に構築されたいくつかの関連する MAPI **IMessage**オブジェクトを処理するサービス プロバイダーによって使用されます。 クライアントまたはプロバイダーは、 [OpenIMsgSession](openimsgsession.md)と**CloseIMsgSession**関数を使用して、メッセージ セッション中には、このようなメッセージの作成をラップします。 メッセージ セッションを開くと、クライアントまたはプロバイダーのポインターに渡します - **IStorage**オブジェクトの新しい**IMessage**を作成する[OpenIMsgOnIStg](openimsgonistg.md)への呼び出しで。 
  
メッセージ セッションは、すべての添付ファイルとメッセージの他のプロパティだけでなく、セッションの期間中に開かれるすべての - 点灯 - **IMessage** **IStorage**オブジェクトの追跡します。 クライアントまたはプロバイダーを呼び出すと**CloseIMsgSession**、これらすべてのオブジェクトを閉じます。 -点灯 - **IStorage**オブジェクト**IMessage**を終了する唯一の方法は、 **CloseIMsgSession**を呼び出すことです。 
  

