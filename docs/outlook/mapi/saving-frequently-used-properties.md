---
title: よく使うプロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e32ed3388e95d32a4857a933fb735d170dd71688
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424554"
---
# <a name="saving-frequently-used-properties"></a>よく使うプロパティの保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
取得に時間とリソースを要し、頻繁にアクセスするデータを格納することで、パフォーマンスを向上させます。 余分なメモリを使用すると、取得を繰り返す方が良いオプションになる場合があります。 このデータを格納するためのキャッシュを作成する場合は、注意と注意が必要です。 キャッシュの設計が不十分な場合、パフォーマンスに悪影響を及ぼす可能性があります。
  
たとえば、ほとんどの対人間メッセージ (IPM) クライアントは、一般的なセッション中に何度もフォルダーの IPM サブツリーを表示および開く必要があります。 これらの各フォルダーのエントリ識別子を格納することで、パフォーマンスを向上させることができます。 
  

