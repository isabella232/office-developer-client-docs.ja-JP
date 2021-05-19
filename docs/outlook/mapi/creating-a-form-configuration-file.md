---
title: フォーム構成ファイルの作成
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
# <a name="creating-a-form-configuration-file"></a>フォーム構成ファイルの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム構成ファイルは、使用するフォーム マネージャーとクライアント アプリケーションの両方にフォームに関する情報を提供します。 フォーム構成ファイルには、メッセージング クライアントで使用するためにフォームによって発行されたプロパティ、フォームによって実装された動詞、フォームでサポートされるプラットフォームなど、フォームの広範な仕様が含まれる。
  
フォーム構成ファイルは、拡張子が .cfg のファイルで、初期化ファイルの形式とWindows形式です。 これは、多数のセクションを含むプレーン テキスト ファイルです。 各セクションは、角かっこで囲まれたセクション名で始まります。 各セクションには、そのセクションに関連する値と設定を定義する 1 つ以上の行が含まれます。 値には、次のいずれかの種類があります。
  
- String
    
- 表示される文字列
    
- プラットフォーム文字列
    
- パス名
    
- 整数
    
- GUID
    
.cfg ファイルのセクションの詳細については、「フォーム構成ファイルの [ファイル形式」を参照してください](file-format-of-form-configuration-files.md)。
  
## <a name="see-also"></a>関連項目



[MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

