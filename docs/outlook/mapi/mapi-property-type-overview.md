---
title: MAPI プロパティの種類の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0bdb1c2a631b80015dbc88dbe5a274c0f9b3050b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600807"
---
# <a name="mapi-property-type-overview"></a>MAPI プロパティの種類の概要
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティの種類は、MAPIDEFS で MAPI によって定義される定数です。プロパティ値の基になるデータ型を示す H ヘッダー ファイル。 MAPI、クライアント アプリケーション、またはサービス プロバイダーによって定義されるプロパティはすべて、次のいずれかの種類を使用します。 
  
プロパティの種類は、プロパティ タグに使用される名前付け規則と同様の名前付け規則に従います。 多くのプロパティ型には、単一値バージョンと複数値バージョンの両方があります。 単一の値を持つプロパティには、1 つの整数や文字列など、その型の 1 つの値が含まれます。 単一の値プロパティを表す定数には、プレフィックス PT_、LONG や STRING8 などの実際の型を表す文字列の 2 つの部分があります。 
  
複数値のプロパティには、その型の複数の値が含まれる。 OLE バリアント配列とは異なり、複数値プロパティのすべての値は同じ型です。 複数値プロパティを表す定数は、MV_FLAG フラグと基本型を表す対応する単一値定数を組み合わせることによって作成されます。 次の 3 つの部分があります。プレフィックスPT_続MV_型を表す文字列が続きます。 たとえば、複数の整数を含むプロパティの型はPT_MV_LONG、複数の文字列の場合はPT_MV_STRING8。
  
次の図は、複数値の整数を表す [SPropValue](spropvalue.md) 構造体の構造を示PT_MV_LONG。 **Value メンバー** が展開され、プロパティ内の整数値の数と、それらの値の配列へのポインターが含まれます。 
  
**複数値プロパティ**
  
![複数値プロパティ](media/amapi_12.gif "複数値プロパティ")
  
複数値のプロパティのサポートは省略可能ですが、MAPI に準拠したコンポーネント間の相互作用が大きいので、クライアントとサービス プロバイダーは両方の種類のプロパティをサポートする必要があります。
  
次の図は **、SPropValue** 構造体に格納されている場所を示す、さまざまなプロパティ型の定数の一覧です。 Value メンバーのサイズ **は** 、特定の型によって異なります。 すべての単一値型に複数値の同等の値があるというのではありません。 
  
**プロパティ タイプ定数**
  
![プロパティ タイプ定数](media/amapi_11.gif "プロパティ タイプ定数")
  
プロパティを操作するクライアントとサービス プロバイダーは、次の 2 つの手順に従う必要があります。
  
1. プロパティが使用可能か使用できないか確認します。
    
2. 使用可能な場合は、プロパティの値を取得します。
    
クライアントまたはサービス プロバイダーは、プロパティの存在のみを確認する必要がある場合があります。それ以外の場合は、特定の値を確認する必要があります。 たとえば、トランスポート プロバイダーには **\_ 、PR SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを処理する 3 つの異なるアクション コースがあります。メッセージを書式設定されたテキストで送信するかどうかを示すブール値です。 **PR メッセージ \_ SEND_RICH_INFO** TRUE に設定されている場合、トランスポート プロバイダーは書式設定されたテキストを送信します。 FALSE に設定されている場合、書式設定されたテキストは送信前に破棄されます。 この **PR_SEND_RICH_INFO** 使用できない場合、トランスポート プロバイダーは、特定のプロバイダーに対する既定の処理に従います。 
  
MAPI では、クライアントまたはサービス プロバイダー PT_UNSPECIFIEDプロパティの種類が不明な場合にプロパティを取得するために使用できる特別なプロパティの種類を定義します。その種類を事前に知らなくてもプロパティを取得するには、クライアントまたはサービス プロバイダーがオブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し、プロパティの識別子と PT_UNSPECIFIED プロパティの種類で構成されるプロパティ タグを渡します。 **GetProps は** 、プロパティの [SPropValue](spropvalue.md) 構造体を返し、プロパティのPT_UNSPECIFIEDを適切な型に置き換える。 **GetProps** を実装するサービス プロバイダーは、この機能をサポートPT_UNSPECIFIED。 
  
一部の MAPI オブジェクトは、自身のオブジェクトであるプロパティをサポートしています。 オブジェクト プロパティの型は、PT_OBJECT。 **IMAPIProp::GetProps** を使用してこれらのプロパティにアクセスする代わりに、クライアントとサービス プロバイダーは通常 [、IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッド、アクセスに適切なインターフェイスを指定する方法、またはプロパティをサポートするオブジェクトのメソッドのいずれかをユーザーにします。 
  
オブジェクト プロパティの値にアクセスするには、オブジェクトのインターフェイスの 1 つを使用する必要があります **。GetProps は** 不適切です。 **GetProps を使用すると**、呼び出し元は SPropValue 構造体を介してプロパティの **値にアクセス** します。 **IMAPIProp::OpenProperty では**、呼び出し元はオブジェクトにアクセスできるインターフェイスへのポインターを取得します。 **OpenProperty は** 、オブジェクト プロパティを取得するために常に使用できます。 オブジェクトのメソッドを呼び出すもう 1 つのオプションは、すべてのオブジェクト プロパティで使用できるとは言えな。 
  
たとえば、すべてのフォルダーは、階層テーブルとコンテンツ テーブルという 2 つのテーブルをサポートします。 これらのテーブルは、フォルダーのプロパティです。プロパティ タグは **、PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) および PR_CONTAINER_CONTENTS **(** [PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) です。 テーブルは、アクセスに **IMAPITable インターフェイスを必要とする** オブジェクトです。 クライアントは、フォルダーの [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出して、階層テーブル、フォルダーの [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) メソッドを呼び出してコンテンツ テーブルにアクセスしたり、フォルダーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを使用していずれかのテーブルにアクセスできます。 **OpenProperty** を呼び出す場合、クライアントはプロパティのプロパティ タグを最初のパラメーターとして渡し、2 番目のパラメーターとしてアクセスに使用するインターフェイスのインターフェイス識別子を渡します。 これらのパラメーター **は、PR_CONTAINER_HIERARCHY****またはPR_CONTAINER_CONTENTS****と** IID_IMAPITable。
  
単一値および複数値のプロパティ型の完全な一覧については、「Property [Types」を参照してください](property-types.md)。 
  
## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)

