---
title: 頻繁に使用されるプロパティの保存
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
# <a name="saving-frequently-used-properties"></a>頻繁に使用されるプロパティの保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
時間とリソースを取得し、頻繁にアクセスするデータを保存することによって、パフォーマンスを向上させます。 その他のメモリを使用すると、繰り返し取得するより良いオプションになることがあります。 このデータを格納するためのキャッシュを作成するときは、注意して使用してください。 適切に設計されていないキャッシュは、パフォーマンスに悪影響を及ぼす可能性があることに注意してください。
  
たとえば、ほとんどの個人間メッセージ (ipm) クライアントは、一般的なセッションの間に、フォルダーの ipm サブツリーを表示して開く必要があります。 これらの各フォルダーのエントリ識別子を格納することによって、パフォーマンスを向上させることができます。 
  

