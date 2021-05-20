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
  
標準プロパティは、MAPI プロパティ、または同じプロパティ識別子で定義された複数の MAPI プロパティを表す仮想プロパティです。 標準プロパティは、コード外のディスカッションやドキュメントで MAPI プロパティの一貫性のある識別を容易にすることを目的とします。 MAPI で定義されたタグ付きプロパティ名とは異なり、標準プロパティ名は MAPI ヘッダー ファイルのグローバル定数として定義されません。
  
## <a name="naming-conventions"></a>名前付け規則

標準プロパティ名は、"プロパティ識別子" を表すプレフィックス "Pid" で始まります。 プロパティがタグ付きプロパティ、数値識別子を持つ名前付きプロパティ、または文字列名を持つ名前付きプロパティのかどうかに応じて、プレフィックスはさらに"PidTag"、"PidLid"、および "PidName" として修飾されます。 たとえば [、PidTagAccount](pidtagaccount-canonical-property.md)は、受信者のアカウント名を指定するタグ付きプロパティ **、PR_ACCOUNT** [(PidTagAccount)、PR_ACCOUNT_A](pidtagaccount-canonical-property.md)[(PidTagAccount)、](pidtagaccount-canonical-property.md)および **PR_ACCOUNT_W** [(PidTagAccount)](pidtagaccount-canonical-property.md)を表します。 [PidLidContacts](pidlidcontacts-canonical-property.md)は **dispidContacts** プロパティ、数値識別子を持ち、メッセージに関連付けられた連絡先の名前を指定する名前付きプロパティを表します。[PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md)は、文字列名を持ち、フィッシングの可能性が高いメッセージをマークする文字列を指定する名前付きプロパティ http://schemas.microsoft.com/outlook/phishingstamp "," を表します。 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>1 つの標準プロパティを使用して類似のプロパティを表す

### <a name="identifying-properties-in-mapi"></a>MAPI のプロパティの識別

MAPI のすべてのプロパティは、署名されていない 16 ビット値であるプロパティ識別子によって識別されます。 プロパティ識別子とプロパティの種類 (もう 1 つの符号なし 16 ビット値) は、プロパティのプロパティ タグを構成します。 
  
MAPI では、プロパティ タグを使用してプロパティを一意に定義します。 **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) や **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber)](pidtagbusiness2telephonenumber-canonical-property.md)など、同じプロパティ タグを持つプロパティは、MAPI では同じプロパティと見なされます。 MAPI が独自のプロパティに対して定義したプロパティ タグの一覧については、「MAPI ヘッダー ファイル Mapitags.h」を参照してください。
  
MAPI はプロパティ識別子を範囲に分割します。 識別子が範囲内にある場合は、その使用と所有権を示します。 タグ付きプロパティのプロパティ識別子は、タグ付きプロパティの0x0001から0x7FFF。 この範囲内には、MAPI 定義プロパティのプロパティ識別子が含まれるので、このプロパティの範囲は0x0001から0x3FFF。 名前付きプロパティのプロパティ識別子は、指定されたプロパティの範囲0x8000から0x8FFF。 
  
名前付きプロパティは、プロパティ セット、および長い ID (LID) (符号なし 32 ビット値)、または文字列によってさらに属性付けされます。 プロパティ セットは、同様の目的で名前付きプロパティのグループを識別する GUID です。 プロパティ セットと LID または文字列名を使用して、名前付きプロパティを取得または設定します。
  
### <a name="property-type"></a>プロパティの種類

識別子とは別に、プロパティは、そのプロパティに対して許可される値の種類を指定するデータ型によって属性付けされます。
  
文字列型のプロパティの場合、基になるプラットフォームでの Unicode のサポートに応じて、プロパティの種類は PT_STRING8 (null 終端の 8 ビット文字列) または PT_UNICODE (null 終端 Unicode 文字列) です。 プロパティは PT_TSTRING 型で定義できます。コンパイル設定に応じて、PT_TSTRING は Unicode をサポートするプラットフォームの Unicode 文字列、ANSI または DBCS をサポートするプラットフォームの PT_STRING8 文字列に既定で定義できます。 文字列型プロパティは、PT_TSTRING、PT_STRING8、および **PT_UNICODE** の 3 つの類似した名前 **(PR_ACCOUNT、PR_ACCOUNT_A、PR_ACCOUNT_W** など) で識別されるのが一般的です。 
  
型に関連するプロパティの種類とマクロの詳細については、「MAPI ヘッダー ファイル Mapidefs.h」を参照してください。
  
### <a name="identifying-similar-properties"></a>類似のプロパティの識別

現在の MAPI プロパティの環境では、プロパティが異なるプロパティ名で公開されているのは珍しいことではありません。そのすべてが同じプロパティ識別子で定義されています。 たとえば、タグ付けされたプロパティ(PR_BUSINESS2_TELEPHONE_NUMBER と **PR_OFFICE2_TELEPHONE_NUMBER)** は、Mapitags.h で同じプロパティ識別子と型を持つとして定義されます。 これら 2 つのプロパティに密接に関連するプロパティは次のとおりです。
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
"_A" 接尾辞を持つプロパティは PT_STRING8 として入力され、"_W" 接尾辞を持つプロパティは"PT_UNICODE" と入力PT_UNICODE。
  
この例の標準プロパティ **である PidTagBusiness2TelephoneNumber** の目的は、1 つの識別子を使用して、すべての MAPI プロパティで一貫した方法で ("Pid" プレフィックスを使用して) このような密接に関連する MAPI プロパティを参照し、容易に行う方法です。 標準プロパティが表す実際の MAPI プロパティを確認するには [、「Mapping Canonical Property Names to MAPI Names」を参照してください](mapping-canonical-property-names-to-mapi-names.md)。 MAPI プロパティが関連付けられている標準プロパティを見つけるには、「MAPPING MAPI Names to [Canonical Property Names」を参照してください](mapping-mapi-names-to-canonical-property-names.md)。
  
## <a name="mapi-support-of-canonical-property-names"></a>標準プロパティ名の MAPI サポート

標準プロパティは実際のプロパティではなく、MAPI ヘッダー ファイルで定義されていないので、コードで標準プロパティ名を使用する必要はありません。代わりに、引き続きコードで MAPI プロパティ名を正確に使用する必要があります。 たとえば、コードの外部PR_BUSINESS2_TELEPHONE_NUMBERと PR_OFFICE2_TELEPHONE_NUMBER を **PidTagBusiness2TelephoneNumber** として参照し、コードで PR_BUSINESS2_TELEPHONE_NUMBERまたは PR_OFFICE2_TELEPHONE_NUMBER を使用できます。 
  
コードで標準プロパティ名を使用する必要がある場合は、まず独自のヘッダー ファイルで定義する必要があります。
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>標準プロパティの名前とExchangeプロトコル仕様

標準名は、他Microsoft Exchange Server Microsoft 製品との通信に使用Exchange Serverプロトコル仕様で参照されます。 プロトコル仕様で参照されるメッセージ オブジェクトプロパティ[Exchange、[MS-OXPROPS] を参照してください](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)。
  
## <a name="see-also"></a>関連項目



[MAPI プロパティ のタグ](mapi-property-tags.md)
  
[MAPI プロパティ識別子の概要](mapi-property-identifier-overview.md)
  
[MAPI プロパティの種類の概要](mapi-property-type-overview.md)

