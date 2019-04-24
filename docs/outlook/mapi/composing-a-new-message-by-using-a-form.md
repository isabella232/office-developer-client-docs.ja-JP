---
title: フォームを使用して新しいメッセージを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335127"
---
# <a name="composing-a-new-message-by-using-a-form"></a>フォームを使用して新しいメッセージを作成する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームを使用して新しいメッセージを作成するには、まず、新しいカスタムメッセージオブジェクトを作成します。
  
 **フォームを使用して新しいメッセージを作成するには**
  
1. フォームマネージャーの[imapiformmgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出して、フォーム情報オブジェクトへのポインターを取得します。これは、 [imapiformmgr: imapiprop](imapiforminfoimapiprop.md)インターフェイスを実装するオブジェクトです。 
    
2. [imapiformmgr:: CreateForm](imapiformmgr-createform.md)を呼び出して、フォーム情報オブジェクトへのポインターを渡します。 **CreateForm**は、適切なフォームサーバーを読み込みます。 さらに、インターフェイス識別子を**CreateForm**に渡して、新しいメッセージへのアクセスに使用するインターフェイスを指定します。 通常、IID_IPersistMessage を**CreateForm**に渡すことによって、 [IPersistMessage: IUnknown](ipersistmessageiunknown.md)を要求します。
    
3. [IPersistMessage:: save](ipersistmessage-save.md)メソッドを呼び出して、新しいメッセージを保存します。 フォームサーバーは、メッセージの作成時に、メッセージの必要なプロパティの値を設定する必要があります。 
    
4. 次の2つの方法のいずれかを使用してメッセージを読み込みます。 [imapiformmgr:: loadform](imapiformmgr-loadform.md)または[imapisession::P repareform](imapisession-prepareform.md)の後に[imapisession:: showform](imapisession-showform.md)を続けます。 これらの戦略の詳細については、「[フォームへのメッセージの読み込み](loading-a-message-into-a-form.md)」を参照してください。
    
> [!NOTE]
> 新しいカスタムメッセージをフォームサーバーに読み込むときに、**そのメッセージに必要な処理中にそのメッセージに関する情報を取得する機会が既にあるため、パフォーマンスが向上する可能性があります。ResolveMessageClass**および**CreateForm**呼び出し。 このため、「[メッセージをフォームに読み込む](loading-a-message-into-a-form.md)」で説明されているように、 **loadform**を呼び出す前に、必要な処理を簡素化できます。 
  

