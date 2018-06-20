---
title: 標準の MAPI プロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2a080b9e6a824e50648a6df0757826f45b5da1f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801336"
---
# <a name="mapi-canonical-properties"></a>標準の MAPI プロパティ

  
  
**適用されます**: Outlook 
  
標準的なプロパティは、MAPI プロパティ、または同じプロパティの識別子を使用して定義されている複数の MAPI プロパティを表す仮想プロパティです。 標準的なプロパティのみ、ディスカッションやコードの外部でのマニュアルで MAPI プロパティの一貫した識別を容易にするためです。 MAPI 定義のタグ付きのプロパティの名前とは異なり、標準のプロパティ名は MAPI ヘッダー ファイルでグローバル定数として定義されていません。
  
## <a name="naming-conventions"></a>名前付け規則

標準のプロパティ名が"Pid"、「プロパティの識別子」を表す接頭辞で始まる かどうかに応じて、プロパティ タグのプロパティや、数値識別子を持つ名前付きプロパティの文字列名を持つ名前付きプロパティ、プレフィックスは、さらに修飾された"PidTag、"として"PidLid、"と"PidName"それぞれ。 たとえば、 [PidTagAccount](pidtagaccount-canonical-property.md)が**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))、 **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) と**PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)) の受信者を指定するタグ付きのプロパティを表しますアカウント名です。[PidLidContacts](pidlidcontacts-canonical-property.md)は、 **dispidContacts**プロパティを数値の識別子を持つし、メッセージに関連付けられている連絡先の名前を指定する名前付きプロパティを表します[PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md)を表す"http://schemas.microsoft.com/outlook/phishingstamp、"名前付きプロパティの文字列の名前を持つし、フィッシング詐欺である可能性があるメッセージにマークを付ける文字列を指定します。 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>1 つの標準的なプロパティを使用して同様のプロパティを表す

### <a name="identifying-properties-in-mapi"></a>MAPI のプロパティを識別します。

MAPI のすべてのプロパティは、符号なしの 16 ビット値であるプロパティの識別子によって識別されます。 プロパティ識別子とプロパティの型 (もう 1 つの符号なし 16 ビット値) は、プロパティ タグのプロパティを構成します。 
  
MAPI は、プロパティを一意に定義するのにプロパティ タグを使用します。 **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) と**PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) のように、同じプロパティ タグのプロパティが同じと見なされますMAPI のプロパティです。 独自のプロパティに定義した MAPI プロパティ タグの一覧は、MAPI のヘッダー ファイル、Mapitags.h を参照してください。
  
MAPI が範囲にプロパティの識別子を分割することに注意してください。 識別子が範囲に該当する場所は、その使用法と所有権を示します。 タグ付きのプロパティのプロパティ識別子は、0x0001 に 0x7FFF の範囲に収まります。 この範囲内で、0x0001 から 0x3FFF の範囲に MAPI 定義のプロパティのプロパティの識別子です。 0x8FFF に 0x8000 からの範囲での秋の名前付きプロパティのプロパティ識別子。 
  
名前付きプロパティは、プロパティを設定して、長い ID (LID)、符号なしの 32 ビット値である、または文字列のいずれかで属性をさらにします。 プロパティ セットは、類似の目的を使用して名前付きプロパティのグループを識別する GUID です。 取得または名前付きプロパティを設定するのには、カバーまたは文字列の名前とプロパティのセットが使用されます。
  
### <a name="property-type"></a>プロパティの種類

、識別子は別にそのプロパティの値の型を指定するデータ型によってプロパティの属性が。
  
型 PT_STRING8 プロパティの場合、基になるプラットフォームでの Unicode のサポートによって、文字列型のプロパティは、(8 ビット文字の null で終わる文字列) または PT_UNICODE (null で終わる Unicode 文字列)。 PT_TSTRING タイプでは、プロパティを定義することができ、または PT_STRING8 文字列を ANSI または DBCS をサポートするプラットフォームに Unicode 文字列、Unicode をサポートしているプラットフォーム用にコンパイルの設定によって PT_TSTRING の既定値です。 文字列型のプロパティが一般的で識別される**PR_ACCOUNT**、 **PR_ACCOUNT_A**、 **PR_ACCOUNT_W**、タイプはなど、3 つの類似した名前 PT_TSTRING、PT_STRING8、および PT_UNICODE それぞれ。
  
プロパティの型と型に関連するマクロの詳細については、MAPI のヘッダー ファイル、Mapidefs.h を参照してください。
  
### <a name="identifying-similar-properties"></a>ようなプロパティを識別します。

現在の MAPI プロパティの横に [別のプロパティ名、同じプロパティの識別子を持つ定義は、すべてのプロパティが公開されているかを検索することも珍しくはありません。 たとえば、タグ付きのプロパティ、 **PR_BUSINESS2_TELEPHONE_NUMBER** **PR_OFFICE2_TELEPHONE_NUMBER**は、同じプロパティの識別子と型を持つ Mapitags.h で定義されます。 密接に関連してこれらの 2 つのプロパティします。
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
PT_STRING8、として"_A"サフィックスを使用してプロパティを入力し、PT_UNICODE として入力された"_W"サフィックスが付いています。
  
この例では、 **PidTagBusiness2TelephoneNumber** 、標準的なプロパティの目的は、1 つの識別子を使用してこのような密接に関連の MAPI プロパティの参照を容易にして、すべての MAPI 経由で一貫した方法 ("Pid"プレフィックスを使用して)プロパティです。 どの標準的なプロパティを表す実際の MAPI プロパティを検索するには、 [MAPI の名前を標準のプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)を参照してください。 MAPI プロパティが関連付けられている標準のプロパティを検索するには、[標準のプロパティ名に MAPI 名前のマッピング](mapping-mapi-names-to-canonical-property-names.md)を参照してください。
  
## <a name="mapi-support-of-canonical-property-names"></a>標準のプロパティ名の MAPI サポート

コードでは、標準のプロパティ名を使用しないでください MAPI ヘッダー ファイルで定義されていない標準的なプロパティが実際のプロパティではないため、代わりに、コードで MAPI プロパティの正確な名前を使用して続行する必要があります。 たとえば、外部コードとして**PidTagBusiness2TelephoneNumber**、 **PR_BUSINESS2_TELEPHONE_NUMBER**および**PR_OFFICE2_TELEPHONE_NUMBER**を参照してください、 **PR_BUSINESS2_TELEPHONE_NUMBER**または**PR_OFFICE2_ のいずれかを使用して、TELEPHONE_NUMBER**のコードにします。 
  
場合は、コードでは、標準のプロパティ名を使用する必要があります、まず、独自のヘッダー ファイルで定義した必要があります。
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>標準のプロパティ名、および Exchange プロトコルの仕様

正規名は、Exchange Server で他のマイクロソフト製品との通信に使用される Microsoft Exchange Server プロトコルの仕様で参照されます。 メッセージ交換プロトコルの仕様によって参照されるオブジェクトのプロパティの詳細については、 [[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI プロパティ タグ](mapi-property-tags.md)
  
[MAPI プロパティ識別子の概要](mapi-property-identifier-overview.md)
  
[MAPI プロパティの型の概要](mapi-property-type-overview.md)

