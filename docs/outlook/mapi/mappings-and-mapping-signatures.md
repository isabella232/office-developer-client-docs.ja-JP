---
title: マッピングとマッピングの署名
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 16f192ae816aba2dd0e34a42fba211c3ef70ba47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801542"
---
# <a name="mappings-and-mapping-signatures"></a>マッピングとマッピングの署名

  
  
**適用されます**: Outlook 
  
サービス プロバイダーは、名前付きプロパティをサポートする場合、id と名前のペアの各セットをマッピングと呼びます。 マッピングの 1 つまたは複数のサービス プロバイダーをサポートできます。 1 つのメッセージ ストア プロバイダー、たとえば、すべてのメッセージ、フォルダー、およびメッセージ ストアのオブジェクト名と、対応する識別子の 1 つのリストを操作するのに**GetIDsFromNames**および**GetNamesFromIDs**メソッドを実装できます。 別のメッセージ ストア プロバイダーは、すべてのフォルダーと、それに含まれるメッセージの 1 つのリストまたはすべてのメッセージとすべてのフォルダーの一意のリストを実装可能性があります。 メッセージごとに固有のマッピングを使用するメッセージ ストア プロバイダーは、指定したプロパティ名のプロパティの識別子がメッセージからを異なるため、フォルダーの内容のテーブルに表示する名前付きプロパティを許可できません。 MAPI では、プロバイダーがシンプルにして、すべてのテーブルを含むオブジェクトの 1 つのリストで、操作をお勧めします。 
  
すべてのマッピングでは、サービス ・ プロバイダーにマッピング署名ことが必要です。 マッピングの署名とは、通常、GUID、一連のプロパティ識別子と、対応する名前を一意に識別するバイナリ値です。 署名のマッピングは、オブジェクトの**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) に格納されます。 サービス プロバイダーは、それが表すマップに変更が加えられるたびに、 **PR_MAPPING_SIGNATURE**プロパティの値を変更しなければなりません。 たとえば、名前または新しい名前に新しい識別子が割り当てられている識別子のペアが追加された場合は、 **PR_MAPPING_SIGNATURE**を更新しなければなりません。 
  
オブジェクトの名前付きプロパティを操作するクライアントでは、比較、およびコピーの操作でオブジェクトの**PR_MAPPING_SIGNATURE**プロパティを使用します。 比較するには、プロパティの識別子の 2 つのオブジェクトに属する、マッピングの署名を使用しないクライアント呼び出す必要があります[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)の両方のオブジェクトの識別子の名前を取得するという名前です。 オブジェクトのマッピングの署名を使用すると、この呼び出しが不要なレンダリングできます。 2 つのオブジェクトの**PR_MAPPING_SIGNATURE**プロパティの値が同じ場合、同じマッピングを使用します。 同じマッピングを使用する識別子を直接比較することができます。 [IMAPIProp::CopyTo](imapiprop-copyto.md)と[IMAPIProp::CopyProps](imapiprop-copyprops.md)を実装するサービス プロバイダーでは、オブジェクトのマッピングの署名のも利用できます。 コピーという名前のオブジェクトのプロパティと、サービス プロバイダーは、元とコピー先のオブジェクトが同じマッピング シグネチャを持つ場合の変換手順を回避できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp: IUnknown](imapipropiunknown.md)


[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)

