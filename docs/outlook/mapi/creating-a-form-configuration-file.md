---
title: フォーム構成ファイルを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425219"
---
# <a name="creating-a-form-configuration-file"></a>フォーム構成ファイルを作成する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム構成ファイルは、使用されているフォームマネージャーとクライアントアプリケーションの両方のフォームに関する情報を提供します。 フォーム構成ファイルには、フォームについての詳細な仕様が含まれています。これには、メッセージングクライアントで使用するためにフォームによって発行されるプロパティ、フォームによって実装される動詞、フォームでサポートされているプラットフォームが含まれます。
  
フォーム構成ファイルは、拡張子が cfg のファイルで、Windows 初期化ファイルに似た形式になっています。 これは、いくつかのセクションがあるプレーンテキストファイルです。 各セクションは、角かっこで囲まれたセクション名で始まります。 各セクションには、そのセクションに関連する値と設定を定義する1つまたは複数の行が含まれています。 値の型は次のいずれかです。
  
- String
    
- 表示される文字列
    
- プラットフォーム文字列
    
- パス名
    
- 整数
    
- GUID
    
cfg ファイルのセクションの詳細については、「[フォーム構成ファイルのファイル形式](file-format-of-form-configuration-files.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI フォームサーバーの開発](developing-mapi-form-servers.md)

