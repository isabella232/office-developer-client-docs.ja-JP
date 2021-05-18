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
  
フォーム サーバーを使用して既存のメッセージをフォームに読み込むには、次のいずれかの方法を使用します。
  
- [IMAPISession::P repareForm](imapisession-prepareform.md)を呼び出してトークンを作成し、次に[IMAPISession::ShowForm](imapisession-showform.md)を呼び出してフォームを表示します。 
    
- [IMAPIFormMgr::LoadForm を呼び出します](imapiformmgr-loadform.md)。 
    
**PrepareForm と** **ShowForm** 戦略の使用は比較的簡単ですが、クライアントに関してモーダルなフォームになります。 これは、フォームが終了するまで **ShowForm** の呼び出しが返されないためです。 フォームを非同期的に処理する必要がある場合は、この戦略を使用しない。 
  
メソッドには **いくつかのパラメーターが必要なので、LoadForm** 戦略の使用は難しくなります。 これらのパラメーターは、適切なコンテキストで適切なフォーム サーバーを起動し、適切なメッセージを表示するようにフォーム マネージャーに指示します。 フォーム サーバーが既に実行されている場合、フォーム マネージャーは、フォーム サーバーの新しいインスタンスを起動せずに、メッセージをフォーム サーバーに読み込む。 
  
起動するフォーム サーバーを指定するには  _、lpszMessageClass_ パラメーターの内容でターゲット サーバーが処理するメッセージ クラスを渡します。 適切なメッセージ クラスは、読み込むメッセージの PR_MESSAGE_CLASS **(** [PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得することで決定できます。 指定したメッセージ クラスのフォーム サーバーがない場合があります。メッセージのスーパークラスに属するメッセージを処理するフォーム サーバーのみです。 そのクラスのメッセージを処理することを特に意図したフォーム サーバーによってのみメッセージを読み込む場合は **、LoadForm** 呼び出しで MAPIFORM_EXACTMATCH フラグを設定します。 詳細については、「MAPI メッセージ [クラス」を参照してください](mapi-message-classes.md)。
  
 **LoadForm** には、ビューアーのメッセージ サイトへのポインターと、ターゲット メッセージ **の PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティと PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティのコンテキストと値が必要です。 
  

