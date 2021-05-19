---
title: 大きな列の操作
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
# <a name="working-with-large-columns"></a>大きな列の操作

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
文字列またはバイナリ プロパティ データを持つ列は、大きく、数千バイトの長さになる可能性があります。 ビューに数百バイトを含む 1 つ以上の列を含めることはできませんが、多くの場合、MAPI を使用すると、テーブルの実装者は値を切り捨て、ほとんどの場合は 255 バイト、頻度は 510 バイトに切り捨てられます。 可能な限り、テーブルの実装者は、プロパティの完全な値をテーブル列に含める必要があります。 推奨される代替手段は、最初の 255 バイトのみを含める方法です。
  
クライアントは、使用しているテーブルが大きな列を切り捨てるかどうかを事前に知る必要があります。 列の長さが 255 バイトまたは 510 バイトの場合、列は切り捨てられたプロパティを表す必要があります。 必要に応じて、クライアントはオブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出すことによって、オブジェクトから切り捨てられた列の完全な値を直接取得できます。 
  
大規模なプロパティを使用して制限を構築するクライアントは、これらの制限がどのように動作するのかについては、テーブル実装者が行う必要があります。 一部のテーブル実装者は、切り捨てられた列で構築される制限を切り捨てられたサイズに基づいて設定し、他の実装者は値全体に基づいて制限を設定できます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

