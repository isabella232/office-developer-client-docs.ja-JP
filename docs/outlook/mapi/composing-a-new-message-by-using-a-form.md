---
title: フォームを使用した新しいメッセージの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f4b9cb00512838e6b54c0cc910b8f7279120db3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799802"
---
# <a name="composing-a-new-message-by-using-a-form"></a>フォームを使用した新しいメッセージの作成

  
  
**適用対象**: Outlook 
  
フォームを使用して、新しいメッセージを作成するのには、まず、新しいカスタム メッセージ オブジェクトを作成します。
  
 **フォームを使用して新しいメッセージを作成するには**
  
1. フォーム情報のオブジェクトへのポインターを取得するために、フォーム マネージャーの[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出すなどを実装するオブジェクト、 [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)インタ フェースです。 
    
2. [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)への呼び出しで、フォームの情報オブジェクトへのポインターを渡します。 **CreateForm**は、フォームの適切なサーバーをロードします。 さらに、新しいメッセージへのアクセスに使用するインターフェイスを指定するのに**CreateForm**にインタ フェース識別子を渡します。 要求する通常は、 [IPersistMessage: IUnknown](ipersistmessageiunknown.md) **CreateForm**に IID_IPersistMessage を渡すことによって。
    
3. [IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出して、新しいメッセージを保存します。 フォーム サーバーは、メッセージを作成するときにメッセージの必要なプロパティの値を設定する必要があります。 
    
4. 2 つの方法のいずれかを使用して、メッセージの読み込み: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)または[IMAPISession::PrepareForm](imapisession-prepareform.md)の後に[IMAPISession::ShowForm](imapisession-showform.md)。 これらの方法の詳細については、[メッセージに、フォームの読み込み](loading-a-message-into-a-form.md)を参照してください。
    
> [!NOTE]
> したがまだ機会があるメッセージについての情報を取得するため、フォームのサーバーに新しいカスタム メッセージを読み込むときにパフォーマンスの向上の機会があるなどのメッセージ クラス-、**に必要な処理中にResolveMessageClass**と**CreateForm**の呼び出しです。 このため、[メッセージに、フォームの読み込み](loading-a-message-into-a-form.md)のトピックで説明する上で**LoadForm**を呼び出す前に必要な処理を簡略化することができます。 
  

