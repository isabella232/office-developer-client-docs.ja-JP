---
title: HELP 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: 検索ボックスに指定したキーワードを使用して HTML ヘルプ ファイルを開きます。
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805522"
---
# <a name="help-function"></a>HELP 関数

**検索**ボックスに指定した*キーワード*では、HTML ヘルプ ファイルを開きます。 
  
## <a name="syntax"></a>構文

ヘルプ ("* * *filename.chm!keyword* * *") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _filename.chm!keyword_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | ヘルプ ファイルの名前と検索対象のキーワードを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

*キーワード*が指定されていない場合、ヘルプ機能は、ヘルプ ファイルの目次のページを開きます。 
  
## <a name="example"></a>例

HELP("visio.chm!shapesheet") 
  
Visio ヘルプ ファイルを開き、キーワード "shapesheet" を含むトピックの一覧を表示します。 
  

