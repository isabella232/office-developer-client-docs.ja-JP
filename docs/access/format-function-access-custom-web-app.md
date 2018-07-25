---
title: Format 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: 指定されたパターンに従って書式設定された値を返します。
ms.openlocfilehash: 974b56ab8e6bc3f97c1931ba67ca9cd08c3511c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798599"
---
# <a name="format-function-access-custom-web-app"></a>Format 関数 (Access カスタム Web アプリ)

指定されたパターンに従って書式設定された値を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **Format** (*Expression*, *Format*) 
  
**Format** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Expression*  <br/> |書式設定する、サポートされるデータ型の式  <br/> |
| *Format*  <br/> | 書式パターン。書式引数には、標準書式文字列 ("C"、"D" など)、または日付や数値用のカスタム文字のパターン ("MMMM dd, yyyy (dddd)" など) として、有効な書式の文字列を含める必要があります。詳細については、「注釈」を参照してください。  <br/> |
   
## <a name="remarks"></a>注釈

*Format*  パラメーターでは、以下のパターンのいずれかに一致する文字列を渡すことができます。 
  
- [標準的な数値書式の文字列](http://msdn.microsoft.com/ja-JP/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [カスタムの数値書式の文字列](http://msdn.microsoft.com/ja-JP/library/0c899ak8%28v=vs.110%29.aspx)
    
- [標準的な日付と時刻の形式の文字列](http://msdn.microsoft.com/ja-JP/library/az4se3k1%28v=vs.110%29.aspx)
    
- [カスタムの日付と時刻の形式の文字列](http://msdn.microsoft.com/ja-JP/library/8kb3ddd4%28v=vs.110%29.aspx)
    
Access 2013 Web アプリケーションの以下の領域では、 **Format** 関数を使用できません。 
  
- テーブル レベルの集計列
    
- UI マクロ
    
- ビュー内の式 (フォーム内など)
    

