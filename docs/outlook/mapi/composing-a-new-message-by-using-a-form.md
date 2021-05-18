---
title: フォームを使用した新しいメッセージの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412801"
---
# <a name="composing-a-new-message-by-using-a-form"></a>フォームを使用した新しいメッセージの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームを使用して新しいメッセージを作成するには、まず新しいカスタム メッセージ オブジェクトを作成します。
  
 **フォームを使用して新しいメッセージを作成するには**
  
1. フォーム マネージャーの [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) メソッドを呼び出して、フォーム情報オブジェクトへのポインター [(IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) インターフェイスを実装するオブジェクト) を取得します。 
    
2. [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)への呼び出しでフォーム情報オブジェクトへのポインターを渡します。 **CreateForm は** 適切なフォーム サーバーを読み込む。 さらに、インターフェイス識別子を **CreateForm** に渡して、新しいメッセージへのアクセスに使用するインターフェイスを指定します。 通常 [、IPersistMessage : IUnknown を](ipersistmessageiunknown.md) CreateForm に渡IID_IPersistMessage **を要求します**。
    
3. [IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出して、新しいメッセージを保存します。 フォーム サーバーは、メッセージを作成するときに、メッセージの必須プロパティの値を設定する必要があります。 
    
4. [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)または[IMAPISession::P repareForm](imapisession-prepareform.md)の後に[IMAPISession::ShowForm](imapisession-showform.md)の 2 つの戦略のいずれかを使用してメッセージを読み込む。 これらの戦略の詳細については、「メッセージをフォームに読み [込む」を参照してください](loading-a-message-into-a-form.md)。
    
> [!NOTE]
> **ResolveMessageClass** 呼び出しと **CreateForm** 呼び出しに必要な処理の間に、メッセージに関する情報 (メッセージ クラスなど) を既に取得する機会が既に存在する可能性が高いので、フォーム サーバーに新しいカスタム メッセージを読み込む際にパフォーマンスが向上する可能性があります。 この理由から **、LoadForm** を呼び出す前に必要な処理を簡略化できます。この処理は、トピック「メッセージをフォームに読み込む」で [説明](loading-a-message-into-a-form.md)されています。 
  

