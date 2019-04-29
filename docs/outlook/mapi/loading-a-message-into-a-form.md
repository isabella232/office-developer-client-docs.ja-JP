---
title: フォームへのメッセージの読み込み
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412416"
---
# <a name="loading-a-message-into-a-form"></a>フォームへのメッセージの読み込み

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームサーバーを使用して既存のメッセージをフォームに読み込むには、次のいずれかの方法を使用します。
  
- 次のように、imapisession を呼び出します。トークンを作成し、次に、フォームを表示するために[apiapisession:: showform](imapisession-showform.md)を実行するには[:P repareform](imapisession-prepareform.md) 。 
    
- [imapiformmgr:: loadform](imapiformmgr-loadform.md)を呼び出します。 
    
**PrepareForm**および**showform**戦略は、比較的簡単ですが、クライアントに関してはモーダルであるフォームが生成されます。 これは、 **showform**の呼び出しが、フォームが終了するまで返されないためです。 フォームを非同期的に処理する必要がある場合は、この方法を使用しないでください。 
  
メソッドにはいくつかのパラメーターが必要なため、 **loadform**戦略を使用することは困難です。 これらのパラメーターによって、フォームマネージャーは適切なコンテキストで適切なフォームサーバーを起動し、適切なメッセージを表示するように指示されます。 フォームサーバーが既に実行されている場合、フォームマネージャーはフォームサーバーの新しいインスタンスを起動せずに、そのメッセージをフォームサーバーに読み込みます。 
  
起動するフォームサーバーを指定するには、ターゲットサーバーによって処理されるメッセージクラスを_lpszmessageclass_パラメーターの内容で渡します。 適切なメッセージクラスは、読み込まれるメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得することによって判断できます。 指定したメッセージクラスのフォームサーバーがなく、メッセージのスーパークラスに属するメッセージを処理するフォームサーバーだけが存在することもあります。 このクラスのメッセージを処理することを目的としたフォームサーバーのみがメッセージを読み込むことを希望する場合は、 **loadform**呼び出しで MAPIFORM_EXACTMATCH フラグを設定します。 詳細については、「 [MAPI メッセージクラス](mapi-message-classes.md)」を参照してください。
  
 また、 **loadform**には、ビューアーのメッセージサイトとビューコンテキストへのポインターと、ターゲットメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) および**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) の値を指定する必要があります。プロパティ.
  

