---
title: 表示テーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435265"
---
# <a name="display-table-implementation"></a>表示テーブルの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルは、1 つ以上のプロパティの表示と編集専用の 1 つ以上のタブ付きプロパティ ページで構成される特別なダイアログ ボックスであるプロパティ シートを表示するために使用されます。 すべての表示テーブルに関連付けられている [のは、IAttach : IMAPIProp インターフェイス](iattachimapiprop.md) の実装です。 [IMAPIProp の実装](imapipropiunknown.md)では、プロパティ シートに表示されるプロパティ データが保持されます。 
  
表示テーブル内の行は、プロパティ シート内のコントロールを表します。 ほとんどのコントロールは、IMAPIProp 実装で管理されている **プロパティに関連付** けできます。 ユーザーが変更可能なコントロールの値を変更すると、対応するプロパティが更新されます。 
  
表示テーブル内の列は、プロパティ シート内の位置、その種類、関連する構造、識別子など、コントロールのプロパティを表します。 必要な表示テーブル列の完全な一覧については、「表示テーブル」 [を参照してください](display-tables.md)。
  
MAPI は、表示テーブルまたは表示テーブルに関連付けられた **IMAPIProp** 実装のプロパティ値を直接読み取って、クライアント アプリケーションのユーザーにプロパティ シートを表示します。 ユーザーがコントロールの値を変更してプロパティ シートを操作すると、MAPI は [IMAPIProp::SetProps](imapiprop-setprops.md) を呼び出して、コントロールの DT_SET_IMMEDIATE フラグが設定されている場合に変更されたコントロールを保存します。 DT_SET_IMMEDIATE フラグが設定DT_SET_IMMEDIATEコントロールの場合、ユーザーが **[OK]** または [今すぐ適用] ボタンをクリックしてダイアログ ボックスを閉じ、プロパティに対する変更 **が保存** されます。 これらのボタンまたは [キャンセル]ボタンのいずれかをクリックすると、MAPI はプロパティ シートをビューから削除します。 
  
MAPI は **、IMAPIProp** 実装で [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出し **、PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求するか [、IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md)などの MAPI に対して行った呼び出しで継承することで、表示テーブルにアクセスできます。
  
最初のアクセス方法は、メッセージング ユーザーまたは配布リストに関する詳細を表示するアドレス帳プロバイダーに求める場合に使用されます。 次の処理が行われます。
  
1. クライアントは [、IAddrBook::Dメソッドを呼び出](iaddrbook-details.md) します。 
    
2. MAPI は、アドレス帳プロバイダーの [IABLogon::OpenEntry](iablogon-openentry.md) メソッドを呼び出して、選択したエントリを表すメッセージング ユーザーにアクセスします。 
    
3. MAPI は、メッセージング ユーザーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出して **、PR_DETAILS_TABLE** プロパティ 、詳細ダイアログ ボックスの表示テーブルを取得します。 
    
4. MAPI は、ユーザーの情報とのやり取りを処理するダイアログ ボックスを表示し、ユーザーが終了するとそのダイアログ ボックスを削除します。 
    
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

