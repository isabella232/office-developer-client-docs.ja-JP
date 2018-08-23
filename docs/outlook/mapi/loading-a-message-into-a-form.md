---
title: フォームへのメッセージ読み込み
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6e65311187ba96abde31a4779ebba371b3d02084
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576499"
---
# <a name="loading-a-message-into-a-form"></a>フォームへのメッセージ読み込み

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームのサーバーを使用してフォームに既存のメッセージをロードするには、次の方法のいずれかを使用します。
  
- トークンを作成する[IMAPISession::PrepareForm](imapisession-prepareform.md)を呼び出すと[IMAPISession::ShowForm](imapisession-showform.md)フォームを表示し、します。 
    
- [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)を呼び出します。 
    
比較的簡単では、 **PrepareForm** 、 **ShowForm**の戦略を使用するが、フォームは、クライアントに対してはモーダルになります。 **ShowForm**への呼び出しは、フォームが終了するまでを返さないためにです。 フォームを非同期的に処理が必要な場合は、この方法を使わないでください。 
  
メソッドがいくつかのパラメーターを必要とするため、 **LoadForm**戦略を使用するがより困難になります。 これらのパラメーターは、適切なコンテキストに適切なフォームのサーバーを起動し、適切なメッセージを表示するフォーム マネージャーに指示します。 フォーム サーバーが既に実行されている場合フォーム マネージャーは、フォームのサーバーの新しいインスタンスを起動しなくてもフォームのサーバーにメッセージを読み込みます。 
  
フォームを起動するサーバーを指定するには、 _lpszMessageClass_パラメーターの内容で、対象サーバーにより処理されるメッセージのクラスを渡します。 読み込むメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを取得することによって、適切なメッセージ クラスを確認できます。 サーバが存在しないフォーム指定したメッセージ クラスのメッセージのスーパークラスに属しているメッセージを処理するフォーム サーバーのみです。 そのクラスのメッセージを処理するもので具体的には、フォーム サーバーのみがメッセージを読み込むことを使用する場合は、 **LoadForm**の呼び出しで MAPIFORM_EXACTMATCH フラグを設定します。 詳細については、 [MAPI メッセージ クラス](mapi-message-classes.md)を参照してください。
  
 **LoadForm**ビューアーのメッセージのサイトとビュー コンテキスト値へのポインターを対象のメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) と**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) も必要です。プロパティです。
  

