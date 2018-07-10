---
title: 新しい MAPI プロパティを定義します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 68e877568565cfcc30b60e9b21f55b7dc1600b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799902"
---
# <a name="defining-new-mapi-properties"></a>新しい MAPI プロパティを定義します。

  
  
**適用されます**: Outlook 
  
にもかかわらず、クライアントとサービスのプロバイダーで使用するため、MAPI によって提供されるプロパティの豊富なは、MAPI は、必要な場合に作成する新しいプロパティを使用できます。 いくつかの新しいパブリック プロパティを定義するための有効なシナリオには、新しいメッセージ クラスと新しいプロパティを作成する独自のメッセージング システムの機能を公開するサービス プロバイダーをサポートするためにプロパティを作成するクライアントが含まれます。
  
通常、既存の MAPI オブジェクトまたはメッセージ クラスの新しいプロパティを定義するのにはサービス ・ プロバイダーに対して無効です。 識別子の標準と形式の要素を設定して、シームレスに混在させるし、一致するユーザーを有効にすると、メッセージング システムの多数のサービスのプロバイダーが、MAPI を使用する場合の主な利点の 1 つ。 非標準プロパティを使用するサービス プロバイダーは他のサービス プロバイダーにも機能しません。 
  
クライアントは、新しいメッセージ クラスのコンテンツのプロパティを作成できます。
  
- メッセージ クラスに固有のコンテンツ プロパティの指定された範囲内のプロパティの識別子を使用しています。
    
    - または、
    
- 名前付きプロパティを使用します。 
    
すべてのサービス プロバイダーが名前付きプロパティをサポートしているために、最初のオプションの使用をお勧めします。 MAPI には、新規のメッセージ クラスに固有のコンテンツ プロパティを使用するクライアントの 2 つの別の範囲が定義されています。
  
- 転送可能なプロパティの 0x6800 に 0x7BFF
    
- 0x7C00 に 0x7FFF nontransmittable のプロパティ
    
プロパティ識別子は、さまざまなベンダー、またはユーザーによって定義されたプロパティとの間の衝突を防ぐための定義済みの範囲である必要があります。 ただし、これらの範囲内のプロパティのユーザーは、プロパティの動作についての前提条件を作成できません。 新しいメッセージ クラスを作成するすべてのクライアントがこれらの範囲へのアクセス権を持つ_xxxx_の識別子を持つプロパティは、1 つのメッセージ クラスの 1 つの動作ともう 1 つのメッセージ クラスの別の動作を意味します。 
  
名前付きプロパティは、特定のプロパティは、メッセージ クラスを一意に保証するために使用されます。 0x8000 の範囲の名前付きプロパティの識別子を開始します。 クライアントでは、1 つまたは複数の名前を定義し、それぞれの名前と識別子を関連付けるには、メッセージ ストアの[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出しています。 名前付きプロパティは、オブジェクトの所有者は、名前付きプロパティをサポートしている場合にのみ、任意のオブジェクトの新しいプロパティを定義するのには、クライアントまたはサービス プロバイダーによって使用できます。 これらのプロパティのユーザー名と識別子にマップするには、 **GetIDsFromNames**と関連する**IMAPIProp**メソッドでは、 [GetNamesFromIDs](imapiprop-getnamesfromids.md)を呼び出します。
  
新規または既存のすべてのプロパティは、一連の定義済みのプロパティの種類を使用してください。 新しいプロパティの種類を追加することはできませんし、既存の型を変更または削除することはできません。 任意の適切な型では、単純で小さななどのプロパティを単一の文字または 16 ビット整数のプロパティを格納できます。 たとえば、 **ulong 型**として整数を格納することができ、 **PT_STRING8**として文字列を格納することができます。 
  
**PT_BINARY**型を使用して、長さのバイト配列を示します。 この種類のプロパティは、オブジェクトに格納できるデータの型を拡張するのに便利です。 シーケンスで送信されるバイト数とデータの意味に関する前提条件は行われません。 クライアント アプリケーションでは、これらのプロパティからデータを読み取る、ときに、データをどのように保存されてから変更することはありません。 クライアントでは、Cpu 間でデータを移動するときの交換のために必要なバイトを実行する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI Property Overview](mapi-property-overview.md)
