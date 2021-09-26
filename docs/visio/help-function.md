---
title: HELP 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
ms.localizationpriority: medium
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: '[検索] ボックスに指定されたキーワードを含む HTML ヘルプ ファイルを開きます。'
ms.openlocfilehash: a4243a9ddbcfda7ef327efd108e1f9954c0fb7b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618883"
---
# <a name="help-function"></a>HELP 関数

[検索] ボックスに指定されたキーワードを含む HTML  *ヘルプ*  ファイルを **開** きます。 
  
## <a name="syntax"></a>構文

HELP(" ** *filename.chm!keyword* ** ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _filename.chm!キーワード_ <br/> |必須  <br/> |**String** <br/> | ヘルプ ファイルの名前と検索対象のキーワードを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

キーワードを  *指定しない*  場合、HELP 関数はヘルプ ファイルのコンテンツ ページを開きます。 
  
## <a name="example"></a>例

HELP("visio.chm!shapesheet") 
  
Visio ヘルプ ファイルを開き、キーワード "shapesheet" を含むトピックの一覧を表示します。 
  

