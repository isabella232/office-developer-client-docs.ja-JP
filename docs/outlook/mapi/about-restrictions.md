---
title: 制限について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322121"
---
# <a name="about-restrictions"></a>制限について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
制限は、ビュー内の行数を、特定の条件に一致する列の値を持つ行だけに制限する方法です。 テーブルに制限を使用すると、さまざまな機会があります。 クライアントアプリケーションでは、制限を使用して、特定のユーザーによって送信されたメッセージのコンテンツテーブルをフィルター処理したり、プロパティをサポートしていない行、またはプロパティを特定の値に設定した行を検索したり、メッセージ。 
  
[imapitable:: Restrict](imapitable-restrict.md)および[imapitable:: FindRow](imapitable-findrow.md)メソッドを使用して、テーブルに制限を設定します。 **Restrict**行を取得せずにテーブルに制限を適用します。 制限を満たす行だけを取得するには、次に示す[IMAPITable:: QueryRows](imapitable-queryrows.md)または類似のメソッドの呼び出しが必要です。 **FindRow**は、制限を適用し、条件に一致するテーブルの最初の行を取得します。 **FindRow**は、通話の間のみ存在する一時的な制限を適用します。**制限**は、より永続的な制限に適用されます。 
  
クライアントによっては、現在の列セットに含まれていない列を使用して制限を構築することができます。 このような制限をサポートすることはオプションであり、それをサポートするテーブル実装者は、特に contents テーブルに対して値を追加します。 Table 実装者は、 **FindRow**呼び出しから、 **Restrict**呼び出しまたは MAPI_E_NOT_FOUND 値から MAPI_E_TOO_COMPLEX 値を返すことができます。 
  
クライアントは、現在の列セットに含まれていない列の制限をプロバイダーがサポートしている場合でも、 [IMAPITable:: SetColumns](imapitable-setcolumns.md)を使用して制限で使用する列を指定することによって、全体的なパフォーマンスが向上することを認識しておく必要があります。.
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

