---
title: MAPI プロパティの種類の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 58dd25f09b76d97fd6441915225756a19f4ec3cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328263"
---
# <a name="mapi-property-type-overview"></a>MAPI プロパティの種類の概要
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティの種類は、mapidefs.h で MAPI によって定義される定数です。プロパティ値の基になるデータ型を示す H ヘッダーファイル。 すべてのプロパティ (MAPI、クライアントアプリケーション、またはサービスプロバイダーによって定義されているかどうか) は、次のいずれかの種類を使用します。 
  
プロパティの種類は、プロパティタグに使用する名前付け規則に似ています。 多くのプロパティの種類には、単一値と複数値の両方のバージョンがあります。 単一の値のプロパティには、1つの整数または文字列などの1つの型の値が含まれています。 単一の値のプロパティを表す定数は、次の2つの部分で構成されます。プレフィックス PT_ と、LONG または STRING8 などの実際の型を表す文字列。 
  
複数値プロパティには、その型の複数の値が含まれています。 OLE バリアント型 (variant) の配列とは異なり、複数値プロパティのすべての値は同じ型です。 複数値プロパティを表すために使用される定数は、MV_FLAG フラグと、それに対応する基本型を表す単一値定数を組み合わせて作成します。 次の3つの部分があります。プレフィックス PT_ の後に MV_ が続き、その後に型を記述する文字列が続きます。 たとえば、複数の整数を含むプロパティの型は PT_MV_LONG で、複数の文字列は PT_MV_STRING8 です。
  
次の図は、PT_MV_LONG 型のプロパティとして、複数値の整数を記述する[spropvalue](spropvalue.md)構造体の構造を示しています。 **Value**メンバーは、プロパティの整数値の数と、それらの値の配列へのポインターを含むように展開されています。 
  
**複数値プロパティ**
  
![複数値プロパティ](media/amapi_12.gif "複数値プロパティ")
  
複数値プロパティのサポートはオプションですが、mapi 準拠のコンポーネント間の相互作用を可能にするため、クライアントとサービスプロバイダーは両方の種類のプロパティをサポートすることをお勧めします。
  
次の図は、さまざまなプロパティの種類の定数を示しています。これは、 **spropvalue**構造に格納されている場所を示しています。 **値**メンバーのサイズは、特定の型によって異なります。 単一値の型には、複数の値が対応しているわけではないことに注意してください。 
  
**プロパティ タイプ定数**
  
![プロパティの種類定数](media/amapi_11.gif "プロパティの種類定数")
  
プロパティを使用するクライアントおよびサービスプロバイダーは、次の2つの手順に従う必要があります。
  
1. プロパティが利用可能かどうかを判断します。
    
2. 可能な場合は、プロパティの値を取得します。
    
クライアントまたはサービスプロバイダーは、プロパティの存在のみをチェックする必要がある場合があります。その他の場合は、特定の値を確認する必要があります。 たとえば、トランスポートプロバイダーには、 **\_PR SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを処理するための3つの異なるコースがあります。これは、メッセージを送信する必要があるかどうかを示すブール値です。書式付きテキスト。 **PR\_SEND_RICH_INFO**が TRUE に設定されている場合、トランスポートプロバイダーは書式設定されたテキストを送信します。 FALSE に設定されている場合は、書式設定されたテキストは送信前に破棄されます。 **PR_SEND_RICH_INFO**が使用できない場合、トランスポートプロバイダーは、特定のプロバイダー向けの既定のアクションの実行に従います。 
  
MAPI は、プロパティの種類が不明な場合にクライアントまたはサービスプロバイダーがプロパティを取得するために使用できる特別なプロパティの種類 PT_UNSPECIFIED を定義します。プロパティを取得するときに、その型を事前に理解していない場合、クライアントまたはサービスプロバイダーは、オブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出し、プロパティの識別子と PT_UNSPECIFIED プロパティの種類で構成されたプロパティタグを渡します。 **GetProps**は、プロパティの[spropvalue](spropvalue.md)構造を返します。 PT_UNSPECIFIED は適切な型に置き換えられます。 **GetProps**を実装するサービスプロバイダーは、PT_UNSPECIFIED をサポートするために必要です。 
  
一部の MAPI オブジェクトは、自身のオブジェクトであるプロパティをサポートしています。 オブジェクトのプロパティの型は PT_OBJECT です。 これらのプロパティにアクセスするには、 **imapiprop:: GetProps**を使用するのではなく、通常、クライアントおよびサービスプロバイダーは、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドをユーザーとして指定し、access の適切なインターフェイスを指定するか、またはオブジェクトに対するメソッドを指定します。プロパティをサポートします。 
  
object プロパティの値にアクセスするには、オブジェクトのインターフェイスの1つを使用する必要があるため、 **GetProps**は適切ではありません。 **GetProps**では、発信者は**spropvalue**構造を使用してプロパティの値にアクセスします。 **imapiprop:: openproperty**を使用すると、呼び出し元は、オブジェクトにアクセスできるインターフェイスへのポインターを取得します。 **openproperty**は、常にオブジェクトプロパティを取得するために使用できます。 その他のオプションは、オブジェクトのメソッドを呼び出すことはできません。すべての object プロパティで使用することはできません。 
  
たとえば、すべてのフォルダーは、階層テーブルと contents テーブルという2つのテーブルをサポートしています。 これらのテーブルは、フォルダーのプロパティです。これらのプロパティタグは、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) および**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) です。 テーブルは、access の**IMAPITable**インターフェイスを必要とするオブジェクトです。 クライアントは、フォルダーの[IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、階層テーブルにアクセスします。フォルダーの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを使用して、コンテンツテーブルにアクセスします。または、フォルダーの[imapiprop:: openproperty](imapiprop-openproperty.md)どちらかのテーブルにアクセスするメソッド。 **openproperty**を呼び出すために、クライアントはプロパティのプロパティタグを最初のパラメーターとして渡し、2番目のパラメーターとしてのアクセスに使用するインターフェイスのインターフェイス識別子を渡します。 これらのパラメーターは、 **PR_CONTAINER_HIERARCHY**または**PR_CONTAINER_CONTENTS**と**IID_IMAPITable**になります。
  
単一値と複数値のプロパティの種類の完全な一覧については、「[プロパティの種類](property-types.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)

