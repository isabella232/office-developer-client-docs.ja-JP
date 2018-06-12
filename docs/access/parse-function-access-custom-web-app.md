---
title: 解析関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798716"
---
# <a name="parse-function-access-custom-web-app"></a>解析関数 (カスタム web アプリケーションのアクセス)

アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。
  
> [!NOTE]
> [!メモ] この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>Syntax

 **解析**(*TextExpression*、*データ型*) 
  
**Parse** 関数には、以下の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *TextExpression*  <br/> |指定したデータ型に解析する、書式設定された値を表す文字列式を指定します。  <br/> |
| *DataType*  <br/> |結果として要求されるデータ型を表すリテラル値。  <br/> |
   
## <a name="remarks"></a>注釈

**Parse** は、文字列から日付/時刻または数値に型を変換する場合にのみ使用します。一般的な型変換では、 **Convert** 関数を使用します。文字列値の解析には、一定のパフォーマンス オーバーヘッドが発生することに注意してください。 
  

