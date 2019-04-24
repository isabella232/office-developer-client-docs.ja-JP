---
title: fielddefinition ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 98584e450bb820dbce05b0f8d2c6d15551586130
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334896"
---
# <a name="fielddefinition-stream-structure"></a>fielddefinition ストリームの構造

**適用対象**: Outlook 2013 | Outlook 2016 
  
fielddefinition ストリーム構造には、ユーザー定義フィールドのフィールド定義、または組み込みフィールドのデータバインド設定のセットのいずれかが含まれています。
  
ユーザー定義のフィールドのフィールド定義が構造に含まれている場合は、プログラムを使用して fielddefinition stream 構造を操作できます。 組み込みフィールドの設定が構造に含まれている場合は、プログラムを使用して fielddefinition 構造を作成または変更しないでください。 組み込みフィールドの設定を維持するには、Microsoft Outlook フォームデザイナーを使用する必要があります。
  
> [!NOTE]
> Outlook では、PropDefV1 と PropDefV2 の2つの形式のフィールド定義をサポートしています。 フィールド定義の PropDefV1 形式には、Flags、VT、DispId、NmidNameLength、nmidname、nameansi、FormulaANSI、validationruleansi、validationruleansi、および erroransi の各データ要素が含まれています。 PropDefV2 形式には、同じ要素と、internaltype 要素と skipblocks 要素が含まれています。 
>
> Outlook では、PropDefV2 フィールド定義形式の FormulaANSI、validationruleansi、および validationruleansi データ要素の Unicode バージョンは保持されません。 これらの要素に ASCII 以外の文字が含まれている場合、Outlook を実行しているコンピューターの ANSI コードページによっては、これらの文字が一貫して解釈されないことがあります。 そのため、これらのデータ要素には、ASCII 文字のみで構成されている文字列値のみを使用する必要があります。 
  
このストリームの Data 要素は、次に示す順序で互いに続けて、リトルエンディアンバイト順に格納されます。
  
- flags: DWORD (4 バイト) は、次の表に示すように、値と意味を含む0個以上のフラグの組み合わせです。
    
    |**フラグ名**|**値**|**説明**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |fielddefinition 構造には、ユーザー定義フィールドの定義が含まれています。  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |このフィールドに連結されているフォームコントロールの場合、[**プロパティ**] ダイアログボックスの [**検証**] タブで、**このフィールドに値**を設定するためのチェックボックスがオンになっている必要があります。  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |このフィールドに連結されているフォームコントロールの場合、[**プロパティ**] ダイアログボックスの [**検証**] タブで [**印刷および名前を付けてこのフィールドを含める**] チェックボックスがオンになっています。  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |このフィールドに連結されているフォームコントロールの場合は、[**プロパティ**] ダイアログボックスの [**値**] タブで、[**この式を自動的に計算**する] チェックボックスがオンになっています。  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |これは型の**組み合わせ**のフィールドであり、**結合フィールドと任意のテキストフラグメント**が、**組み合わせの数式フィールド**ダイアログボックスで選択されている各オプションと共にあります。  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |このフィールドは型の**組み合わせ**であり、[**複合式フィールド**] ダイアログボックスで選択されている次のオプションを無視して、最初の空では**ないフィールドのみを表示**します。  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |このフラグは Outlook では使用されませんが、すべてのユーザー定義フィールド定義に含まれています。  <br/> |
   
- VT: WORD (2 バイト)。これは、 [varenum](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx)列挙の定数であるフィールドのデータ型です。 
    
- DispId: フィールドのディスパッチ識別子 (DWORD) (4 バイト)。 ユーザー定義フィールドの場合、値は0になります。
    
- NmidNameLength: WORD (2 バイト)。 nmidname 配列内の要素の数。
    
- nmidname: WCHAR の配列。 ユーザー定義のフィールド定義の場合、これはフィールド名の Unicode (utf-16) 表現です。 この配列の数は、NmidNameLength と同じです。
    
- nameansi: [PackedAnsiString](packedansistring-stream-structure.md) stream 構造。 これは、フィールド名の ANSI 表現です。 
    
- FormulaANSI: PackedAnsiString stream 構造。 これは、フィールドの計算式を ANSI 表現で表したものです。 このフィールドは、このフィールドに連結されているフォームコントロールの [**プロパティ**] ダイアログボックスの [**値**] タブの [**初期値**] セクションに表示されます。 
    
- validationruleansi: PackedAnsiString stream 構造。 これは、フィールドの検証式の ANSI 表現です。 このフィールドは、このフィールドにバインドされているフォームコントロールの [**プロパティ**] ダイアログボックスの [**入力規則**] タブで、[入力規則の**数式**] テキストボックスに表示されます。 
    
- validationtextansi: PackedAnsiString stream 構造。 これは、フィールドの検証エラーテキストを ANSI で表現したものです。 このフィールドにバインドされているフォームコントロールの [**プロパティ**] ダイアログボックスの [**検証**] タブで**検証が失敗した場合は、このメッセージを表示**するテキストボックスに表示されます。 
    
- erroransi: PackedAnsiString stream 構造。 Outlook では、この要素は使用されません。この要素は空の文字列に設定する必要があります。
    
- internaltype: DWORD (4 バイト) (フィールドの内部型)。 この data 要素は、フィールド定義の形式が PropDefV2 の場合にのみ存在します。 internal 型は、次のいずれかの値です。各値は、ユーザー定義フィールドの [**新しいフィールド**] ダイアログボックスの型に対応します。 
    
    |**内部型名**|**値**|**[**新しいフィールド**の対応する種類] ダイアログボックス**|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |.0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1-d  <br/> |**数値** <br/> |
    |iTypePercent  <br/> |pbm-2  <br/> |**Percent** <br/> |
    |通貨  <br/> |1/3  <br/> |**通貨** <br/> |
    |iTypeBool  <br/> |2/4  <br/> |**はい/いいえ** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**日付/時刻** <br/> |
    |iTypeDuration  <br/> |シックス  <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7  <br/> |**** そして、[**複合式フィールド**] ダイアログボックスで選択されている次のオプションを無視して、最初の空では**ないフィールドのみを表示**します。  <br/> |
    |iTypeFormula  <br/> |~  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |i-9  <br/> |この型は、ユーザー定義フィールドには使用されません。  <br/> |
    |iTypeVariant  <br/> |個  <br/> |この型は、ユーザー定義フィールドには使用されません。  <br/> |
    |iTypeFloatResult  <br/> |#  <br/> |この型は、ユーザー定義フィールドには使用されません。  <br/> |
    |iTypeConcat  <br/> |個  <br/> |**** 組み合わせ、[**フィールド**の結合] ダイアログボックスで選択された [その他] オプションを使用して、**結合フィールドとテキストフラグメント**を指定します。  <br/> |
    |iTypeKeywords  <br/> |スリー  <br/> |**キーワード** <br/> |
    |iTypeInteger  <br/> |第  <br/> |**Integer** <br/> |
   
- skipblocks: 1 つ以上の[skipblocks](skipblock-stream-structure.md)ストリーム構造。 この data 要素は、フィールド定義の形式が PropDefV2 の場合にのみ存在します。 フィールド定義の形式が PropDefV2 の場合、データ系列には、少なくとも1つの skipblock 構造体、Size data 要素を0とする skipblock 構造体、およびこの skipblock 構造を開始して終了する必要があります。 
    
   skipblock 構造の目的は、skipblock シリーズでの相対位置に依存します。 フィールド定義が PropDefV2 形式の場合、最初の構造体が終端構造ではない (Size data 要素が0より大きい) 場合、Outlook は最初の skipblock 構造を想定して、フィールド名を Unicode (utf-16) で指定します。 
    
   > [!IMPORTANT]
   > 最初の skipblock が終端構造である場合、nameansi data 要素を使用してフィールド名を決定します。 この文字列に ASCII 以外の文字が含まれている場合、Outlook を実行しているコンピューターの ANSI コードページによっては、これらの文字が一貫して解釈されないことがあります。 このような不整合を防ぐには、少なくとも、フィールド名に非 ASCII 文字が含まれている場合は、作成するフィールド定義に最初の skipblock を指定してください。 
  
   フィールド定義形式の将来のバージョンで、fielddefinition ストリームに追加のデータが導入されている場合は、このデータを skipblock シリーズに追加の skipblock ストリーム構造体として格納することができます。Size data 要素が0に等しい。 以前のバージョンの Outlook では、このような skipblock 構造を終了することなく、それらの不要な skipblock 構造を無視しても、サポートされているすべてのブロックを正しく処理することができます。
    
## <a name="see-also"></a>関連項目

- [Outlook のアイテムとフィールド](outlook-items-and-fields.md)
- [Stream 構造体](stream-structures.md)
- [propertydefinition ストリームの構造](propertydefinition-stream-structure.md)

