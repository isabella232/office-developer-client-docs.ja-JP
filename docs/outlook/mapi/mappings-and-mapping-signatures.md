---
title: マッピングとマッピングの署名
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: da1a4fe3027d4bf914e93c1000d37bb73e7875db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595750"
---
# <a name="mappings-and-mapping-signatures"></a>マッピングとマッピングの署名

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーが名前付きプロパティをサポートしている場合、識別子と名前のペアの各セットはマッピングと呼ばれます。 サービス プロバイダーは、1 つのマッピングまたは複数のマッピングをサポートできます。 つまり、たとえば、1 つのメッセージ ストア プロバイダーは、すべてのメッセージ、フォルダー、およびメッセージ ストア オブジェクトに対して **GetIDsFromNames** メソッドと **GetNamesFromIDs** メソッドを実装して、名前と対応する識別子の 1 つのリストを操作できます。 別のメッセージ ストア プロバイダーは、フォルダーごとに 1 つのリストを持ち、その中に含まれるメッセージを持つ場合や、すべてのメッセージとフォルダーごとに一意のリストを実装する場合があります。 すべてのメッセージに対して一意のマッピングを使用するメッセージ ストア プロバイダーは、指定されたプロパティ名に対して、プロパティ識別子がメッセージごとに異なるので、フォルダーコンテンツ テーブルに名前付きプロパティを表示することはできません。 MAPI では、プロバイダーが単純な状態を維持し、テーブルを含むすべてのオブジェクトに対して 1 つのリストで操作を行う必要があります。 
  
マッピングごとに、サービス プロバイダーはマッピング署名を指定する必要があります。 マッピング署名は、一連のプロパティ識別子と対応する名前を一意に識別するバイナリ値 (通常は GUID) です。 マッピング署名は、オブジェクトのプロパティ ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md) **)** PR_MAPPING_SIGNATUREに格納されます。 サービス プロバイダーは、それが表すマッピングに変更 **PR_MAPPING_SIGNATURE** プロパティの値を変更する必要があります。 たとえば、新 **PR_MAPPING_SIGNATURE** が名前に割り当てられている場合、または新しい名前と識別子のペアが追加されている場合は、新しい識別子を更新する必要があります。 
  
オブジェクトの名前付きプロパティを操作するクライアントは、比較 **および** コピー操作PR_MAPPING_SIGNATUREオブジェクトのプロパティを使用します。 2 つのオブジェクトに属する名前付きプロパティ識別子を比較するには、マッピング署名を使用していないクライアントは、両方のオブジェクトで [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) を呼び出して、各識別子の名前を取得する必要があります。 オブジェクトのマッピング署名を使用すると、この呼び出しが不要になります。 2 つのオブジェクトのプロパティの値が同 **PR_MAPPING_SIGNATURE、同** じマッピングが使用されます。 同じマッピングを使用する識別子を直接比較できます。 [IMAPIProp::CopyTo](imapiprop-copyto.md)と[IMAPIProp::CopyProps](imapiprop-copyprops.md)を実装するサービス プロバイダーは、オブジェクトのマッピング署名を利用できます。 名前付きプロパティをオブジェクト間でコピーする場合、サービス プロバイダーは、ソース オブジェクトと変換先オブジェクトが同じマッピング署名を持つ場合、変換手順を回避できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)

