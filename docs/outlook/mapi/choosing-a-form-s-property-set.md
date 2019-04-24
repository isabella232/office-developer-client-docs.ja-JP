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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332061"
---
# <a name="choosing-a-forms-property-set"></a>フォームのプロパティ セットの選択

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームサーバーを実装するときは、メッセージクラスに必要な情報の各要素にプロパティを設定する必要があります。 これらのプロパティは、定義済みの MAPI プロパティにすることも、定義するカスタムプロパティにすることもできます。 プロパティの使用の詳細については、「 [MAPI プロパティの概要](mapi-property-overview.md)」を参照してください。
  
フォーム構成ファイルには、フォームサーバーがクライアントアプリケーションで公開するプロパティのリストが含まれていますが、これはフォームサーバーで使用されるプロパティのリスト全体である必要はありません。 通常、クライアントアプリケーションは公開されているプロパティを使用して、ユーザーがフォルダー内のメッセージを並べ替えたり、何らかの方法でインターフェイスをカスタマイズしたりできるようにします。
  
MAPI には、ほとんどのアプリケーションに十分な、定義済みのプロパティセットが多数あります。 ただし、カスタムメッセージクラスに MAPI で定義されていないプロパティが必要になる場合もあります。 カスタムプロパティを使用して、フォームサーバーがサポートする必要のある特別な情報について、MAPI で事前定義されたプロパティのセットを拡張できます。
  
カスタムプロパティを定義するには、次のいずれかの方法を使用できます。
  
- プロパティの名前を選択し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを使用して、プロパティタグを取得します。 このメソッドを呼び出す[imapiprop](imapipropiunknown.md)インターフェイスは、メッセージが作成されたときにフォームサーバーに渡される[IMessage](imessageimapiprop.md)ポインターから取得します。 プロパティ名はワイド文字文字列である必要があることに注意してください。 
    
- カスタムプロパティタグを自分で定義します。 カスタムプロパティタグは、範囲0x6800 から0x7bff にする必要があります。 この範囲のプロパティは、メッセージクラスに固有のものです。
    
カスタムプロパティの定義の詳細については、「[新しい MAPI プロパティの定義](defining-new-mapi-properties.md)」を参照してください。
  
> [!NOTE]
> メッセージテキストを持つフォームサーバーは、通常、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを使用して格納します。 フォームサーバーで**PR_RTF_COMPRESSED**を使用する場合は、リッチテキストをサポートしていないクライアントによってメッセージが読み取られた場合に備えて、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティにメッセージテキストのテキストのみのバージョンが含まれていることを確認する必要があります。Format (RTF) メッセージテキスト。 
  
## <a name="see-also"></a>関連項目

- [MAPI フォームサーバーの開発](developing-mapi-form-servers.md)

