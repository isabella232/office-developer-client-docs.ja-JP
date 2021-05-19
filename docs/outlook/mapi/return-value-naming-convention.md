---
title: 戻り値の名前付け規則
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423616"
---
# <a name="return-value-naming-convention"></a>戻り値の名前付け規則

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPICODE。H ヘッダー ファイルには、クライアントまたはサービス プロバイダーがインターフェイス メソッドの実装から返す値、または呼び出しから返される可能性がある値の多くが含まれています。
  
警告とエラーの条件を表すコードは、プレフィックス MAPI、アンダースコア、およびコードの種類を示す W または E で始まる別の名前付け規則に従います。 残りのコードは、条件を記述する短い文字列です。 文字列内の各単語はアンダースコアで区切ります。 たとえば、呼び出しで要求MAPI_E_TOO_COMPLEX処理できないというエラー値が表示されます。 警告の値MAPI_W_PARTIAL_COMPLETION呼び出しが成功したが、問題が発生したかどうかを示します。 操作の一部だけが正常に完了しました。
  

