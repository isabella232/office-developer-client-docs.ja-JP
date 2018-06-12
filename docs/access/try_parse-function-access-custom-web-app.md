---
title: Try_Parse 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: 指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798756"
---
# <a name="tryparse-function-access-custom-web-app"></a>Try_Parse 関数 (カスタム web アプリケーションのアクセス)

指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。
  
> [!NOTE]
> [!メモ] この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>Syntax

 **Try_Parse**(*TextExpression*、*データ型*) 
  
**Try_Parse** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *TextExpression*  <br/> |指定したデータ型に解析する、書式設定された値を表す文字列式を指定します。  <br/> |
| *DataType*  <br/> |*TextExpression*を解析するためにデータを入力します。  <br/> |
   
## <a name="remarks"></a>解説

**Try_Parse** は、文字列型から日付/時刻型および数値型への変換にのみ使用します。一般的な型変換では、引き続き **Convert** を使用します。 
  

