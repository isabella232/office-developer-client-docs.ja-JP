---
title: マッピングとマッピングの署名
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410015"
---
# <a name="mappings-and-mapping-signatures"></a>マッピングとマッピングの署名

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダーが名前付きプロパティをサポートしている場合、識別子と名前のペアの各セットは、マッピングと呼ばれます。 サービスプロバイダーは、1つまたは複数のマッピングをサポートできます。 たとえば、1つのメッセージストアプロバイダーでは、すべてのメッセージ、フォルダー、およびメッセージストアオブジェクトの**getidsfromnames**および**GetNamesFromIDs**メソッドを実装して、名前とそれに対応する識別子のリストを1つのリストで操作できます。 別のメッセージストアプロバイダーは、フォルダーとその中に含まれるメッセージごとに1つのリストを持つことができます。または、すべてのメッセージとすべてのフォルダーに固有のリストを実装します。 メッセージストアプロバイダーは、特定のプロパティ名に関して、すべてのメッセージに一意のマッピングを使用して、名前付きプロパティをフォルダーコンテンツテーブルに表示しないようにする必要があります。 MAPI では、プロバイダーがシンプルに保持し、テーブルを含むすべてのオブジェクトに対して単一のリストを使用することをお勧めします。 
  
すべてのマッピングについて、サービスプロバイダーはマッピング署名を指定する必要があります。 マッピングシグネチャはバイナリ値 (通常は GUID) で、一連のプロパティ識別子とそれに対応する名前を一意に識別します。 署名のマッピングは、オブジェクトの**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) プロパティに格納されます。 サービスプロバイダーが表すマッピングが変更されたときは、その**PR_MAPPING_SIGNATURE**プロパティの値を変更する必要があります。 たとえば、新しい識別子が名前または新しい名前に割り当てられ、識別子のペアが追加されている場合は、 **PR_MAPPING_SIGNATURE**を更新する必要があります。 
  
オブジェクトの名前付きプロパティを操作するクライアントは、 **PR_MAPPING_SIGNATURE**プロパティを比較およびコピー操作で使用します。 2つのオブジェクトに属する名前付きプロパティ識別子を比較するには、マッピングシグネチャを使用していないクライアントは、両方のオブジェクトで[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)を呼び出して、各識別子の名前を取得する必要があります。 オブジェクトのマッピングシグネチャを使用すると、この呼び出しが不要になることがあります。 2つのオブジェクトの**PR_MAPPING_SIGNATURE**プロパティの値が同じ場合は、同じマッピングを使用します。 同じマッピングを使用する識別子は、直接比較できます。 [imapiprop:: CopyTo](imapiprop-copyto.md)および[imapiprop:: copyprops](imapiprop-copyprops.md)を実装するサービスプロバイダーは、オブジェクトのマッピングシグネチャを利用することもできます。 オブジェクト間で名前付きプロパティをコピーする場合、サービスプロバイダーは、移行元とコピー先のオブジェクトが同じマッピング署名を持っている場合に、変換手順を回避できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)

