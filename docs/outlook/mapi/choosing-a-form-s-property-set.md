---
title: フォームのプロパティ セットを選択します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0ff8d9f1ae25c55d66847b8c0e5e66c406dfdfba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586152"
---
# <a name="choosing-a-forms-property-set"></a>フォームのプロパティ セットを選択します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム サーバーを実装する場合は、個々 のメッセージ クラスに必要な情報のプロパティを持つ必要があります。 これらのプロパティは、MAPI のプロパティ、定義済みまたはカスタム プロパティを定義することができます。 プロパティの使用についての詳細については、 [MAPI プロパティの概要](mapi-property-overview.md)を参照してください。
  
フォーム構成ファイルには、クライアント アプリケーションが使用するため、フォームのサーバーを公開するプロパティの一覧が含まれているが、全体、フォームのサーバーで使用されるプロパティの一覧にこれがありません。 通常、クライアント アプリケーションは、フォルダー内のメッセージを並べ替える、または何らかの方法では、そのインターフェイスをカスタマイズするのにユーザーを有効にするのに公開されたプロパティを使用します。
  
MAPI には、ほとんどのアプリケーションで十分に定義済みのプロパティの大規模なセットがあります。 ただし、カスタム メッセージ クラスが MAPI が定義されていないプロパティをどのようにしなければならない場合があります。 カスタム プロパティを使用するには、フォーム サーバーがサポートするのに必要が特別な情報をすべてのプロパティの定義済みの MAPI のセットを拡張します。
  
カスタム プロパティを定義するのには次の方法のいずれかを使用することができます。
  
- プロパティの名前を選択し、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを使用して、プロパティ タグを取得します。 [IMAPIProp](imapipropiunknown.md)インターフェイスを使用するには、このメソッドを呼び出してメッセージを作成するときにフォームのサーバーに渡される[IMessage](imessageimapiprop.md)ポインターに由来します。 プロパティ名は、ワイド文字の文字列である必要があります注意してください。 
    
- カスタム プロパティ タグを自分で定義します。 カスタム プロパティ タグは、0x7BFF から 0x6800 の範囲でなければなりません。 メッセージ クラスは、この範囲のプロパティを特定します。
    
カスタム プロパティを定義する方法の詳細については、[新しい MAPI プロパティを定義する](defining-new-mapi-properties.md)を参照してください。
  
> [!NOTE]
> 多くの場合、メッセージ テキストを持つフォームのサーバーでは、そこに格納するのに ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) である**PR_RTF_COMPRESSED**プロパティを使用します。 フォーム サーバーは、 **PR_RTF_COMPRESSED**を使用する場合にも確認してください ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティにメッセージのテキストのテキストのみのバージョンが含まれている結果のメッセージがリッチ テキストをサポートしていないクライアントによって読み取られた場合にテキスト形 (式 RTF) メッセージのテキストです。 
  
## <a name="see-also"></a>関連項目

- [MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

