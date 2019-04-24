---
title: フォーム構成ファイルのファイル形式
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d07d88d7b8b892a82832f91989e322ea3b32e040
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334826"
---
# <a name="file-format-of-form-configuration-files"></a>フォーム構成ファイルのファイル形式

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム構成ファイルは、フォーム開発者がフォームを定義するために作成した形式のファイルです。
  
フォーム構成ファイルはフォームマネージャーによってフォームの読み込みに使用されるため、フォーム構成ファイルを使用して各フォームを定義する必要があります。 フォーム構成ファイルには、拡張子が cfg である必要があります。 このファイルは、Windows 初期化ファイル (.ini ファイル) の一般的な構文に従います。 

このセクションは、指定されたセクションに分かれており、各セクションには一連のエントリと値が含まれています。 値の型は、string、表示された文字列、プラットフォーム文字列、パス、整数、またはグローバル一意識別子 ( **GUID**) のいずれかです。 フォーム構成ファイルは、テキストファイルの保存が可能なテキストエディターまたはワープロを使用して作成できます。
  

