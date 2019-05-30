---
title: MAPI 標準プロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2fc605c57936765f43d7a6941dcc8d40d058db2f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540477"
---
# <a name="mapi-canonical-properties"></a>MAPI 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準プロパティは、MAPI プロパティ、または同じプロパティ識別子で定義された複数の MAPI プロパティを表す仮想プロパティです。 標準プロパティは、コード外のディスカッションやドキュメントでの MAPI プロパティの一貫した識別を容易にすることを目的としています。 MAPI で定義されたタグ付きプロパティ名とは異なり、標準プロパティ名は MAPI ヘッダーファイルでグローバル定数として定義されません。
  
## <a name="naming-conventions"></a>名前付け規則

標準プロパティ名は、"Pid" というプレフィックスで始まります。これは "プロパティ識別子" を表します。 プロパティがタグ付きプロパティであるか、数値識別子を持つ名前付きプロパティであるか、または文字列名を持つ名前付きプロパティであるかに応じて、プレフィックスはそれぞれ "PidTag"、"PidLid"、および "PidName" として修飾されます。 たとえば、 [PidTagAccount](pidtagaccount-canonical-property.md)は、受信者の**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))、 **PR_ACCOUNT_A** (PidTagAccount[](pidtagaccount-canonical-property.md))、 **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)) を表します。アカウント名。[PidLidContacts](pidlidcontacts-canonical-property.md)は、 **dispidcontacts**プロパティを表します。これは、メッセージに関連付けられている連絡先の名前を表す数値識別子を持つ名前付きプロパティです。と[PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md)は、http://schemas.microsoft.com/outlook/phishingstamp文字列名を持つ名前付きプロパティを表し、フィッシングである可能性が高いメッセージをマークする文字列を指定します。 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>1つの標準プロパティを使用して類似のプロパティを表す

### <a name="identifying-properties-in-mapi"></a>MAPI でのプロパティの識別

MAPI のすべてのプロパティは、署名されていない16ビット値であるプロパティ識別子によって識別されます。 プロパティの識別子とプロパティの型 (別の符号なしの16ビット値) は、プロパティのプロパティタグを構成します。 
  
MAPI では、プロパティタグを使用して、プロパティを一意に定義します。 **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) および**PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) など、同じプロパティタグを持つプロパティは同一であると見なされます。MAPI のプロパティ。 MAPI が独自のプロパティに対して定義したプロパティタグの一覧については、「MAPI ヘッダーファイル Mapitags」を参照してください。
  
MAPI はプロパティ識別子を範囲に分割することに注意してください。 範囲内の識別子は、その使用と所有権を示します。 タグ付きプロパティのプロパティ識別子は、0x0001 の範囲に含まれています。 この範囲内では、MAPI で定義されたプロパティのプロパティ識別子が0x0001 から0x3FFF の範囲に入ります。 名前付きプロパティのプロパティ識別子は、0x8000 から0x8FFF の範囲になります。 
  
名前付きプロパティは、さらにプロパティセットによって、または、符号なしの32ビット値である long ID (LID)、または文字列のいずれかによって属性されます。 プロパティセットは、同じ目的を持つ名前付きプロパティのグループを識別する GUID です。 プロパティセットと LID または文字列名は、名前付きプロパティを取得または設定するために使用されます。
  
### <a name="property-type"></a>プロパティの種類

識別子とは別に、プロパティは、そのプロパティに使用できる値の型を指定するデータ型によって属性されます。
  
基になるプラットフォームでの Unicode のサポートに応じて、string 型のプロパティの場合、プロパティの型は PT_STRING8 (null で終了する8ビット文字列) または PT_UNICODE (null で終わる Unicode 文字列) です。 プロパティは PT_TSTRING 型で定義できます。コンパイル設定に応じて、Unicode をサポートするプラットフォーム用の Unicode 文字列、または ANSI または DBCS をサポートする PT_STRING8 文字列に対して、PT_TSTRING の既定値を指定できます。 文字列型 (string) 型のプロパティは、 **PR_ACCOUNT**、 **PR_ACCOUNT_A**、 **PR_ACCOUNT_W**などの3つの類似する名前で識別されます。これは、それぞれ PT_TSTRING、PT_STRING8、および PT_UNICODE の種類です。
  
種類に関連するプロパティの種類とマクロの詳細については、「MAPI ヘッダーファイル Mapidefs.h」を参照してください。
  
### <a name="identifying-similar-properties"></a>類似したプロパティを識別する

現在の MAPI プロパティの風景では、プロパティが異なるプロパティ名で公開されていて、すべてのプロパティが同じプロパティ識別子で定義されていることを検出するのは珍しいことではありません。 たとえば、 **PR_BUSINESS2_TELEPHONE_NUMBER**と**PR_OFFICE2_TELEPHONE_NUMBER**というタグ付きプロパティは、Mapitags プロパティの識別子と種類が同じになるように定義されています。 これらの2つのプロパティに密接に関連しています。
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
"_ A" サフィックスが付いたプロパティは PT_STRING8 として入力され、"_ W" サフィックスを持つプロパティは PT_UNICODE として入力されます。
  
この例では、標準プロパティの**PidTagBusiness2TelephoneNumber**を使用して、このように密接に関連する mapi プロパティを1つの識別子を使用して参照し、一貫性のある方法 ("Pid" プレフィックスを使用) をすべての mapi で容易に参照することができます。プロパティ. 標準プロパティが表す実際の MAPI プロパティを検索する方法については、「[標準プロパティ名から Mapi 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)」を参照してください。 MAPI プロパティが関連付けられている標準プロパティを検索するには、「 [Mapi 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)」を参照してください。
  
## <a name="mapi-support-of-canonical-property-names"></a>標準プロパティ名の MAPI サポート

標準プロパティは実際のプロパティではなく、MAPI ヘッダーファイルで定義されていないため、コードで標準プロパティ名を使用しないでください。代わりに、コードで MAPI プロパティの正確な名前を使用する必要があります。 たとえば、コードの外部で**PR_BUSINESS2_TELEPHONE_NUMBER**と**PR_OFFICE2_TELEPHONE_NUMBER**を**PidTagBusiness2TelephoneNumber**として参照して、 **PR_BUSINESS2_TELEPHONE_NUMBER**または PR_OFFICE2_ を使用することができます。 **** コード内の TELEPHONE_NUMBER。 
  
コードで正規のプロパティ名を使用する必要がある場合は、最初に独自のヘッダーファイルで定義する必要があります。
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>標準プロパティ名と Exchange プロトコル仕様

正規名は、Exchange Server が他の Microsoft 製品と通信するために使用する Microsoft Exchange Server protocol の仕様で参照されています。 Exchange プロトコル仕様によって参照されるメッセージオブジェクトプロパティの詳細については、「 [[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI プロパティタグ](mapi-property-tags.md)
  
[MAPI プロパティ識別子の概要](mapi-property-identifier-overview.md)
  
[MAPI プロパティの種類の概要](mapi-property-type-overview.md)

