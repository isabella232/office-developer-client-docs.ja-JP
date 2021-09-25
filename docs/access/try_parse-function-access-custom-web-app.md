---
title: Try_Parse関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: 指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。
ms.openlocfilehash: ee4007dee0b000f8093c61a095df91a4dd56fc66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588407"
---
# <a name="try_parse-function-access-custom-web-app"></a>Try_Parse関数 (Access カスタム Web アプリ)

指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

 **Try_Parse** (*TextExpression*, *DataType*) 
  
**Try_Parse** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *TextExpression*  <br/> |指定したデータ型になっているか解析される対象の、書式設定された値を表すテキスト式。  <br/> |
| *DataType*  <br/> |*TextExpression* を解析するデータ型です。  <br/> |
   
## <a name="remarks"></a>注釈

**Try_Parse** は、文字列型から日付/時刻型および数値型への変換にのみ使用します。一般的な型変換では、引き続き **Convert** を使用します。 
  

