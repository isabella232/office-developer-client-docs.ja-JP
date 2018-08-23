---
title: MAPI プロパティの型の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ce3cd37247f37c4e70adb07769f00b2df07307a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801428"
---
# <a name="mapi-property-type-overview"></a>MAPI プロパティの型の概要
  
**適用対象**: Outlook 
  
プロパティの型は、MAPIDEFS では、MAPI によって定義されている定数です。H ヘッダー ファイルのプロパティ値の基になるデータ型を示す。 すべてのプロパティは、MAPI、クライアント アプリケーション、またはサービス ・ プロバイダーに定義されているかどうかを使用して、これらの種類のいずれかです。 
  
プロパティの型は、次のような名前付け規則のプロパティ タグを使用に設定します。 多くのプロパティの種類には、単一値と複数値の両方のバージョンがインストールされています。 1 つの値を持つプロパティには、1 つの整数や文字列などの型の 1 つの値が含まれています。 単一値のプロパティを表すために使用する定数には、2 つの部分: プレフィックス PT_ と時間の長い、STRING8 など、実際の型を記述する文字列。 
  
複数値プロパティには、その型の 1 つ以上の値が含まれています。 OLE バリアント型の配列とは異なりは、同じ種類の複数値を持つプロパティに含まれる値です。 複数値を持つプロパティを表すために使用する定数は、対応する 1 つの値を表す定数基本型と、MV_FLAG フラグを組み合わせることによって作成されます。 次の 3 つの部分があります: MV_ の後に PT_ というプレフィックスの後に型を表す文字列。 たとえば、複数の整数を格納しているプロパティの型は、PT_MV_LONG、PT_MV_STRING8 は、複数の文字列をします。
  
次の図は、複数値の整数では、PT_MV_LONG の種類のプロパティを記述する[SPropValue](spropvalue.md)構造体の構造を示します。 **値**のメンバーは、プロパティとそれらの値の配列へのポインターに整数値の数のカウントを含むように拡張されます。 
  
**複数値プロパティ**
  
![複数値のプロパティ](media/amapi_12.gif "複数値のプロパティ")
  
複数値をサポートするプロパティは省略可能、MAPI は、クライアントとサービス ・ プロバイダーをサポートして両方の種類のプロパティのため、有効に MAPI 準拠のコンポーネント間の対話をよりことをお勧めします。
  
次の図では、すべて**SPropValue**構造体に格納されている場所を示すさまざまなプロパティ型の定数の一覧表示されます。 **値**のメンバーのサイズは、特定のタイプによって異なります。 対応する複数値があるすべての単一値の型に注意してください。 
  
**プロパティ タイプ定数**
  
![プロパティの型の定数](media/amapi_11.gif "プロパティの型の定数")
  
クライアントとサービス プロバイダーのプロパティは、2 つの手順に従う必要があります。
  
1. プロパティが使用可能または使用できないかを確認します。
    
2. 可能な場合、プロパティの値を取得します。
    
クライアントまたはサービス プロバイダーが必要なプロパティの存在をチェックだけ場合があります。それ以外の場合は、特定の値を確認する必要があります。 たとえば、トランスポート プロバイダーが処理のためのアクションの 3 つの異なるコースをある、 **PR\_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティ、メッセージで送信されるかどうかを示すブール値書式設定されたテキストです。 場合**PR\_SEND_RICH_INFO**は、トランスポート プロバイダーは、TRUE に設定すると、書式設定されたテキストを送信します。 FALSE に設定されている場合は、伝送する前に書式設定されたテキストが破棄されます。 **PR_SEND_RICH_INFO**では、トランスポート プロバイダーは、次のようにアクションのどのような場合は、その既定コースは特定のプロバイダーにします。 
  
MAPI は、PT_UNSPECIFIED は、クライアントまたはサービス プロバイダーは、プロパティの型が不明の場合は、プロパティを取得するために使用できる特殊なプロパティ型を定義します。型の事前知識がないプロパティを取得するには、クライアントまたはサービス プロバイダーはオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すし、プロパティ タグのプロパティの識別子と、PT_UNSPECIFIED プロパティのデータ型を渡します。 **GetProps**に、PT_UNSPECIFIED を適切な型に置き換えてプロパティの[SPropValue](spropvalue.md)構造体を返します。 **GetProps**を実装するサービス プロバイダーは、PT_UNSPECIFIED をサポートする必要があります。 
  
MAPI オブジェクトのいくつかは、オブジェクトを自体はプロパティをサポートします。 PT_OBJECT 型は、オブジェクトのプロパティであります。 通常これらのプロパティ、クライアント、サービス プロバイダーにアクセスするのには**IMAPIProp::GetProps**を使用する代わりにユーザーのいずれかの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッド、オブジェクトのアクセス、またはメソッドの適切なインターフェイスを指定します。プロパティをサポートします。 
  
オブジェクトのプロパティの値にアクセスするため、オブジェクトの使用するインタ フェースのいずれかの**GetProps**が適切ではありませんが含まれます。 **GetProps**、呼び出し元がプロパティの値をアクセス**SPropValue**構造体を使用。 **IMAPIProp::OpenProperty**では、呼び出し元は、オブジェクトにアクセスできるインターフェイスへのポインターを取得します。 **OpenProperty**は、オブジェクトのプロパティを取得するために常に使用できます。 すべてのオブジェクト プロパティを使用して、オブジェクトのメソッドを呼び出して、他のオプションが得られません。 
  
たとえば、すべてのフォルダーには、2 つのテーブル、階層テーブルおよび内容のテーブルがサポートされています。 これらのテーブルには、フォルダーのプロパティプロパティ タグは、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) および**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) です。 テーブルは、アクセスの**IMAPITable**インターフェイスを必要とするオブジェクトです。 クライアントは、階層テーブルの内容のテーブル、またはフォルダーの[IMAPIProp::OpenProperty にアクセスするためのフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドにアクセスするためのフォルダーの[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出すことができます。](imapiprop-openproperty.md)いずれかのテーブルにアクセスするメソッドです。 **OpenProperty**を呼び出すには、クライアントは、最初のパラメーターと 2 番目のパラメーターとしてのアクセスに使用するインターフェイスのインターフェイス識別子とプロパティのプロパティ タグを渡します。 これらのパラメーターは、 **PR_CONTAINER_HIERARCHY**または**PR_CONTAINER_CONTENTS**と**IID_IMAPITable**になります。
  
単一値および複数値プロパティの型の完全なリストは、[プロパティの型](property-types.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)

