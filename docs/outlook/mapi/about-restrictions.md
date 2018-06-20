---
title: 制限について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d7294527fcd557ae2d4824b9a3215ff464f62c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799607"
---
# <a name="about-restrictions"></a>制限について

  
  
**適用されます**: Outlook 
  
制限は、特定の条件に一致する列の値を持つ行のみをビューでの行の数を制限する方法です。 テーブルでの制限を使用するための多くのさまざまなチャンスがあります。 クライアント アプリケーションの制限を使用、たとえば、特定の人物がプロパティをサポートしていないか、特定の値にプロパティを設定している行を検索するか、内で重複した受信者を検索するに送信されるメッセージの内容のテーブルにフィルターを適用するのには、メッセージ。 
  
テーブルに制限を設定するのには、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドと[IMAPITable::FindRow](imapitable-findrow.md)メソッドが使用されます。 **だけに制限する**には、任意の行を取得することがなく、テーブルに制限が適用されます。 制限に一致する行だけを取得するには、 [IMAPITable::QueryRows](imapitable-queryrows.md)または同様のメソッドへの後続の呼び出しが必要です。 **FindRow**は、制限を適用し、条件に一致するテーブルの最初の行を取得します。 **FindRow** **だけに制限する**には永続的な制限が適用されますが、呼び出しの間のみ存在は、一時的な制限を適用します。 
  
一部のクライアントは、現在の列ではなく設定された列を使用して制限を構築できます。 オプションは、このような制限をサポートしているし、それをサポートしているテーブルの実装者は、特に内容のテーブルの場合、値を追加します。 サポートしていないテーブルの実装では、**制限**の呼び出しまたは**FindRow**の呼び出しから MAPI_E_NOT_FOUND 値から MAPI_E_TOO_COMPLEX 値を返すことができます。 
  
クライアントは、場合でも、プロバイダーは、現在の列のセットにない列の制限をサポートして、それらを取得する全体的なパフォーマンスを向上させる[IMAPITable::SetColumns](imapitable-setcolumns.md)では、その制限に使用する列を指定することで対応する必要があります。.
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

