---
title: Parse 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。
ms.openlocfilehash: e09478cee26accd8e316d3de36d8034f0ca02526
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631539"
---
# <a name="parse-function-access-custom-web-app"></a>Parse 関数 (Access カスタム Web アプリ)

アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

 **Parse** (*TextExpression*, *DataType*) 
  
**Parse** 関数には、以下の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *TextExpression*  <br/> |指定したデータ型になっているか解析される対象の、書式設定された値を表すテキスト式。  <br/> |
| *DataType*  <br/> |結果として要求されるデータ型を表すリテラル値。  <br/> |
   
## <a name="remarks"></a>注釈

**Parse** は、文字列から日付/時刻または数値に型を変換する場合にのみ使用します。一般的な型変換では、 **Convert** 関数を使用します。文字列値の解析には、一定のパフォーマンス オーバーヘッドが発生することに注意してください。 
  

