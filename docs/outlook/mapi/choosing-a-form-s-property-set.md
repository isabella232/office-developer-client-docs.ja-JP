---
title: フォームのプロパティ セットの選択
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407194"
---
# <a name="choosing-a-forms-property-set"></a>フォームのプロパティ セットの選択

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム サーバーを実装する場合は、メッセージ クラスで必要な情報ごとにプロパティを持つ必要があります。 これらのプロパティには、定義済みの MAPI プロパティを指定するか、定義するカスタム プロパティを指定できます。 プロパティの操作の詳細については、「MAPI プロパティの概要 [」を参照してください](mapi-property-overview.md)。
  
フォーム構成ファイルには、クライアント アプリケーションが使用するためにフォーム サーバーが公開するプロパティの一覧が含まれるが、フォーム サーバーで使用されるプロパティのリスト全体である必要はない。 クライアント アプリケーションは通常、公開されたプロパティを使用して、ユーザーがフォルダー内のメッセージを並べ替え、または何らかの方法でインターフェイスをカスタマイズできます。
  
MAPI には、ほとんどのアプリケーションで十分な定義済みのプロパティの大きなセットがあります。 ただし、MAPI で定義されていないプロパティがカスタム メッセージ クラスに必要な場合があります。 カスタム プロパティを使用して、フォーム サーバーがサポートする必要がある特別な情報に対して MAPI 定義済みのプロパティセットを拡張できます。
  
カスタム プロパティを定義するには、次のいずれかの方法を使用できます。
  
- プロパティの名前を選択し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを使用してプロパティ タグを取得します。 この [メソッドを呼び出す IMAPIProp](imapipropiunknown.md) インターフェイスは、メッセージの作成時にフォーム サーバーに渡される [IMessage](imessageimapiprop.md) ポインターから取得されます。 プロパティ名はワイド文字の文字列である必要があります。 
    
- カスタム プロパティ タグを自分で定義します。 カスタム プロパティ タグは、カスタム プロパティ タグの0x6800 0x7BFF。 この範囲のプロパティは、メッセージ クラス固有です。
    
カスタム プロパティの定義の詳細については、「新しい [MAPI プロパティの定義」を参照してください](defining-new-mapi-properties.md)。
  
> [!NOTE]
> メッセージ テキストを含むフォーム サーバーは、多くの場合、PR_RTF_COMPRESSED **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを使用して保存します。 フォーム サーバーで **PR_RTF_COMPRESSED** を使用する場合は、リッチ テキスト形式 (RTF) メッセージ テキストをサポートしていないクライアントが結果のメッセージを読み取る場合に備え **、PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティにメッセージ テキストのテキスト専用バージョンが含まれている必要があります。 
  
## <a name="see-also"></a>関連項目

- [MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

