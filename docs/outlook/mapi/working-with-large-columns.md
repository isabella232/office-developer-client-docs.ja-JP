---
title: 大規模な列の使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a191a8551d425d7e8b3b9a281936a4a0e2dfd587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804220"
---
# <a name="working-with-large-columns"></a>大規模な列の使用

  
  
**適用されます**: Outlook 
  
文字列またはバイナリ プロパティ データを持つ列が大きくなる可能性のある膨大な数のバイト長です。 ビューで、数百バイトの 1 つまたは複数の列を含む多くの場合実用的ではありません、ために、MAPI には、テーブル実装側は、255 バイトには多くの場合、使用頻度は少ない 510 バイトに値を切り詰めますが有効にします。 可能な限り、テーブルの実装者は、テーブルの列にプロパティの完全な値を含める必要があります。 最初の 255 バイトを含めることをお勧めします。
  
クライアントは、使用しているテーブルに行が切り捨てられますかどうか事前に知ることはできません。 列の長さが 255 であるか、510 バイトである場合、列が切り捨てられたプロパティを表すことを想定してください。 必要に応じて、クライアント直接値を取得完全切り捨てられた列のオブジェクトからオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すことによって。 
  
大きなプロパティの制限を作成するクライアントは、対応することがテーブルの実装方法にこれらの制限を次のように動作します。 はずです。 いくつかのテーブルの実装では、切り捨てられた列全体の値を基に他のユーザー中に切り捨てられたサイズに基づく構築された制限を使用できます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

