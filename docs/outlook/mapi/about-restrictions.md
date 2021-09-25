---
title: 制限について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 127e88eef946a4cf9417adbc1860a492cfe825cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557009"
---
# <a name="about-restrictions"></a>制限について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
制限は、ビュー内の行数を、特定の条件に一致する列の値を持つ行にのみ制限する方法です。 テーブルで制限を使用するには、さまざまな機会があります。 クライアント アプリケーションは、たとえば、特定のユーザーが送信したメッセージのコンテンツ テーブルをフィルター処理したり、プロパティをサポートしていない行やプロパティを特定の値に設定した行を検索したり、メッセージ内で重複する受信者を検索したりするために制限を使用できます。 
  
[IMAPITable::Restrict](imapitable-restrict.md)メソッドと[IMAPITable::FindRow](imapitable-findrow.md)メソッドを使用して、テーブルに制限を設定します。 **Restrict** は、行を取得せずにテーブルに制限を適用します。 制限を満たす行のみを取得するには [、IMAPITable::QueryRows](imapitable-queryrows.md) または同様のメソッドへの後続の呼び出しが必要です。 **FindRow** は制限を適用し、条件に一致する表の最初の行を取得します。 **FindRow** は一時的な制限を適用します。これは呼び出しの期間中のみ存在しますが **、Restrict** は、より永続的な制限を適用します。 
  
一部のクライアントでは、現在の列セットに含めされていない列を使用して制限を作成できます。 このような制限のサポートはオプションであり、特にコンテンツ テーブルの場合は、値の追加をサポートするテーブル実装者です。 サポートしていないテーブル実装者は **、Restrict** 呼び出しMAPI_E_TOO_COMPLEXまたは **FindRow** 呼び出しから MAPI_E_NOT_FOUND値を返します。 
  
クライアントは、プロバイダーが現在の列セットではない列に対する制限をサポートしている場合でも [、IMAPITable::SetColumns](imapitable-setcolumns.md)の制限で使用する列を指定することで、全体的にパフォーマンスが向上します。
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

