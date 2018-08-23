---
title: 表示テーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 07ad94c423c3be425dc905dc578f55ad2c467a95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799921"
---
# <a name="display-table-implementation"></a>表示テーブルの実装

  
  
**適用対象**: Outlook 
  
表示テーブルを使用して、プロパティ シートでは、1 つまたは複数のタブ付きプロパティ ページを表示して、おそらく 1 つまたは複数のプロパティを編集するのには専用の特別なダイアログ ボックスで構成されるを表示します。 関連付けられているテーブルは、すべてのディスプレイで、 [IAttach: IMAPIProp](iattachimapiprop.md)インターフェイスの実装です。 [IMAPIProp](imapipropiunknown.md)の実装では、プロパティ シートに記載されているプロパティのデータを保持します。 
  
ディスプレイ テーブル内の行は、プロパティ シートのコントロールを表します。 ほとんどのコントロールは、 **IMAPIProp**の実装と管理プロパティに関連付けることができます。 ユーザーは、変更可能なコントロールの値を変更するときは、対応するプロパティが更新されます。 
  
表示テーブルの各列は、プロパティ シート、種類、関連付けられている構造体、および識別子の位置など、コントロールのプロパティを表します。 必要な表示のテーブルの列の一覧については、[テーブルの表示](display-tables.md)を参照してください。
  
MAPI を参照してプロパティ値表示のテーブルに関連付けられている**IMAPIProp**実装とは、表示された表から直接、クライアント アプリケーションのユーザーにプロパティ シートが表示されます。 ユーザーは、プロパティ シートでは、コントロールで値を変更する MAPI が呼び出され、コントロールの DT_SET_IMMEDIATE フラグが設定されている場合は、変更されたコントロールを保存するのには[IMAPIProp::SetProps](imapiprop-setprops.md)です。 DT_SET_IMMEDIATE フラグが設定されていないコントロールは、ユーザーが、[ **OK** ] または [**今すぐ適用**] ボタンをクリックしてダイアログ ボックスを閉じるときに、プロパティへの変更は保存されます。 これらのボタンまたは **[キャンセル**] ボタンのいずれかをクリックすると、MAPI は、ビューからプロパティ シートを削除します。 
  
**IMAPIProp**実装では、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すと、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを要求するか、継承することで MAPI が、表示テーブルへのアクセスを取得します。[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)など、MAPI に対して行った呼び出しです。
  
最初のアクセス方法は、ユーザーまたは配布リストのメッセージに関する詳細を表示するアドレス帳プロバイダーが求められたときに使用されます。 次の処理が行われます。
  
1. クライアントは、 [IAddrBook::Details](iaddrbook-details.md)メソッドを呼び出します。 
    
2. MAPI では、選択したエントリを表すメッセージのユーザーにアクセスするためのアドレス帳プロバイダーの[IABLogon::OpenEntry](iablogon-openentry.md)メソッドを呼び出します。 
    
3. MAPI では、 **PR_DETAILS_TABLE**プロパティで、[詳細情報] ダイアログ ボックスに表示された表を取得するために、メッセージング ユーザーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 
    
4. MAPI では、情報を含むユーザーの相互作用を処理します] ダイアログ ボックスを表示し、ユーザーが終了したときに削除します。 
    
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

