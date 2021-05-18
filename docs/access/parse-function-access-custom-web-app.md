---
title: Parse 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411135"
---
# <a name="parse-function-access-custom-web-app"></a>Parse 関数 (Access カスタム Web アプリ)

アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **Parse** (*TextExpression*, *DataType*) 
  
**Parse** 関数には、以下の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *TextExpression*  <br/> |指定したデータ型になっているか解析される対象の、書式設定された値を表すテキスト式。  <br/> |
| *DataType*  <br/> |結果として要求されるデータ型を表すリテラル値。  <br/> |
   
## <a name="remarks"></a>注釈

**Parse** は、文字列から日付/時刻または数値に型を変換する場合にのみ使用します。一般的な型変換では、 **Convert** 関数を使用します。文字列値の解析には、一定のパフォーマンス オーバーヘッドが発生することに注意してください。 
  

