---
title: 大きな列を処理する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420424"
---
# <a name="working-with-large-columns"></a>大きな列を処理する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
文字列またはバイナリのプロパティデータを持つ列は大規模である可能性があり、多くの場合、長さが何千バイトになることがあります。 ビュー内の1つまたは複数の列が表示されている場合、多くの場合、MAPI を使用すると、テーブル実装者は値を切り捨てることができます。通常は255バイト、それよりも510バイトになります。 テーブルの実装では、可能であれば、テーブルの列にプロパティの完全な値を含める必要があります。 推奨される代替方法は、最初の255バイトのみを含めることです。
  
クライアントは、使用しているテーブルが大きな列を切り捨てているかどうかを事前に知ることはできません。 列の長さが255または510バイトの場合、列が切り捨てられたプロパティを表すと想定する必要があります。 必要に応じて、オブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出すことにより、切り捨てられた列の完全な値をクライアントが直接取得することができます。 
  
大規模なプロパティを使用して構築するクライアントは、これらの制限がどのように機能するかについて、テーブルの実装者に依存していることに注意する必要があります。 表の実装によっては、切り捨てられたサイズに基づいて、切り捨てられた列を使用して作成された制限を使用している場合や、値全体を基準とする場合があります。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

