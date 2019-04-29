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
  
表示テーブルは、プロパティシートを表示するために使用されます。このダイアログボックスには、1つまたは複数のプロパティを表示して編集するための専用のタブ付きプロパティページから構成されます。 すべての表示テーブルに関連付けられているのは、 [iattach: imapiprop](iattachimapiprop.md)インターフェイスの実装です。 [imapiprop](imapipropiunknown.md)の実装は、プロパティシートに表示されるプロパティデータを保持します。 
  
表示テーブル内の行は、プロパティシートのコントロールを表します。 ほとんどのコントロールは、 **imapiprop**の実装で管理されるプロパティに関連付けることができます。 ユーザーが変更可能なコントロールの値を変更すると、対応するプロパティが更新されます。 
  
表示テーブル内の列は、コントロールのプロパティを表します。たとえば、プロパティシート内の位置、種類、関連付けられた構造体、識別子などがあります。 必要な表示テーブル列の完全な一覧については、「[表の表示](display-tables.md)」を参照してください。
  
MAPI では、表示テーブルに関連付けられている**imapiprop**実装のプロパティ値、または直接表示テーブルからプロパティ値を読み取ることによって、クライアントアプリケーションのユーザーにプロパティシートが表示されます。 ユーザーがプロパティシートを使用してコントロールの値を変更すると、MAPI は[imapiprop:: setprops](imapiprop-setprops.md)を呼び出して、コントロールの DT_SET_IMMEDIATE フラグが設定されている場合は、変更されたコントロールを保存します。 DT_SET_IMMEDIATE フラグが設定されていないコントロールでは、ユーザーが **[OK** ] または [**今すぐ適用**] ボタンをクリックしてダイアログボックスを閉じたときに、プロパティの変更が保存されます。 これらのボタンのいずれか、または **[キャンセル**] ボタンがクリックされると、MAPI はプロパティシートをビューから削除します。 
  
MAPI は、 **imapiprop**の実装で[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求するか、またはこのプロパティを継承することによって、表示テーブルへのアクセスを取得します。[imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)など、MAPI に対して行った通話。
  
最初のアクセス方法は、アドレス帳プロバイダーがメッセージングユーザーまたは配布リストに関する詳細を表示するように求められた場合に使用します。 次の処理が行われます。
  
1. クライアントが[IAddrBook::D etails](iaddrbook-details.md)メソッドを呼び出します。 
    
2. MAPI は、アドレス帳プロバイダーの[IABLogon:: openentry](iablogon-openentry.md)メソッドを呼び出して、選択されたエントリを表すメッセージングユーザーにアクセスします。 
    
3. MAPI は、メッセージングユーザーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_DETAILS_TABLE**プロパティ、[詳細] ダイアログボックスの表示テーブルを取得します。 
    
4. MAPI はダイアログボックスを表示し、ユーザーの情報の操作を処理して、ユーザーが終了したときに削除します。 
    
## <a name="see-also"></a>関連項目



[MAPI サービスプロバイダー](mapi-service-providers.md)

