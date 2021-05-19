---
title: Try_Parse関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: 指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427529"
---
# <a name="try_parse-function-access-custom-web-app"></a>Try_Parse関数 (Access カスタム Web アプリ)

指定したアプリケーションのカルチャのデータ型にテキスト値を解析します。変換が無効な場合は Null を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **Try_Parse** (*TextExpression*, *DataType*) 
  
**Try_Parse** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *TextExpression*  <br/> |指定したデータ型になっているか解析される対象の、書式設定された値を表すテキスト式。  <br/> |
| *DataType*  <br/> |*TextExpression* を解析するデータ型です。  <br/> |
   
## <a name="remarks"></a>注釈

**Try_Parse** は、文字列型から日付/時刻型および数値型への変換にのみ使用します。一般的な型変換では、引き続き **Convert** を使用します。 
  

