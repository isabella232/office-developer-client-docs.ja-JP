---
title: FieldDefinition ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 775dc1b5fdcf40867f67fbab25879bd97de24f4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800046"
---
# <a name="fielddefinition-stream-structure"></a>FieldDefinition ストリームの構造

**適用されます**: Outlook 
  
FieldDefinition ストリームの構造体には、ユーザー定義のフィールドのフィールドの定義または組み込みのフィールドのデータ バインディングの設定のセットのいずれかが含まれています。
  
構造体には、ユーザー定義のフィールドのフィールド定義が含まれている場合にプログラムを使用して、FieldDefinition ストリームの構造を操作できます。 プログラムで作成または構造体には、組み込みのフィールドの設定が含まれている場合は、FieldDefinition 構造体を変更しないようにします。 組み込みのフィールドには、このような設定を維持するために Microsoft Outlook のフォーム デザイナーを使用してください。
  
> [!NOTE]
> Outlook には、フィールドの定義の 2 つの形式がサポートされています: PropDefV1 と PropDefV2。 PropDefV1 形式フィールドの定義にはには、次のデータ要素が含まれています: フラグ、VT、DispId、NmidNameLength、NmidName、NameANSI、FormulaANSI、ValidationRuleANSI、ValidationTextANSI、および ErrorANSI。 PropDefV2 形式には、同じ要素や、InternalType と SkipBlocks の要素が含まれています。 
>
> Outlook では、PropDefV2 フィールドの定義の形式で FormulaANSI、ValidationRuleANSI、および ValidationTextANSI のデータ要素の Unicode バージョンは保持されません。 場合はこれらの要素には、非 ASCII 文字が含まれている、これらの文字が Outlook を実行しているコンピューターの ANSI コード ページによって一貫性がない解釈可能性があります。 したがって、これらのデータ要素の ASCII 文字のみで構成される文字列の値のみを使用してください。 
  
このストリーム内のデータ要素は、以下に指定した順序で互いのすぐ後、リトル エンディアンのバイト順で格納されます。
  
- フラグ: DWORD (4 バイト) の値と意味は次の表に記載されている 1 つ以上のフラグの組み合わせです。
    
    |**フラグ名**|**値**|**説明**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |FieldDefinition 構造体には、ユーザー定義フィールドの定義が含まれています。  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |このフィールドに連結されたフォーム コントロールの**プロパティ**] ダイアログ ボックスの [**検証**] タブでの**値がこのフィールドに必要な**チェック ボックスが選択されます。  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |フォーム コントロールのチェック ボックスは、このフィールドにバインドされている**印刷用には、このフィールドを含めると名前を付けて保存****のプロパティ**] ダイアログ ボックスの [**検証**] タブで選択しました。  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |このフィールドに連結されたフォーム コントロールの**プロパティ**] ダイアログ ボックスの [**値**] タブで**次の数式を自動的に計算**のチェック ボックスが選択されます。  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |これは、フィールドの種類**の組み合わせ**との**組み合わせの式のフィールド**] ダイアログ ボックスで選択した**フィールドの組み合わせすべてを相互に**オプションがあります。  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |このフィールドは、型**の組み合わせ**のと**組み合わせ数式フィールド**] ダイアログ ボックスで**最初の空ではないフィールドだけ、うちの表示**オプションを選択します。  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Outlook でこのフラグが設定されていないが、すべてのユーザー定義フィールドの定義に含まれます。  <br/> |
   
- VT: ワード (2 バイト)、 [VARENUM](http://msdn.microsoft.com/en-us/library/system.runtime.interopservices.varenum.aspx)の列挙体の定数は、フィールドのデータ型です。 
    
- DispId: DWORD (4 バイト) で、フィールドのディスパッチ識別子。 ユーザー定義フィールドの値が 0 を使用します。
    
- NmidNameLength: ワード (2 バイト)、NmidName 配列内の要素の数。
    
- NmidName: wchar 型の配列。 ユーザー定義フィールドの定義では、これは、Unicode (utf-16) の形式のフィールド名です。 この配列の数は NmidNameLength になります。
    
- NameANSI: [PackedAnsiString](packedansistring-stream-structure.md)ストリームの構造体。 これは、ANSI の形式のフィールド名です。 
    
- FormulaANSI: PackedAnsiString ストリームの構造体。 これは、フィールドの計算式の ANSI 表現です。 このフィールドに連結されたフォーム コントロールの [**プロパティ**] ダイアログ ボックスの [**値**] タブの [**初期値**] セクションに表示されます。 
    
- ValidationRuleANSI: PackedAnsiString ストリームの構造体。 これは、フィールドの入力規則の数式の ANSI 表現です。 このフィールドに連結されたフォーム コントロールの [**プロパティ**] ダイアログ ボックスの [**検証**] タブで**入力規則の数式**をテキスト ボックスに表示されます。 
    
- ValidationTextANSI: PackedAnsiString ストリームの構造体。 これは、フィールドの入力規則のエラー テキストの ANSI 表現です。 このフィールドに連結されたフォーム コントロールの [**プロパティ**] ダイアログ ボックスの [**検証**] タブで **、検証が失敗した場合は、このメッセージを表示する**ためのテキスト ボックスに表示されます。 
    
- ErrorANSI: PackedAnsiString ストリームの構造体。 Outlook では、この要素は使用しません。空の文字列には、この要素を設定する必要があります。
    
- InternalType: DWORD (4 バイト) で、フィールドの内部の型。 このデータ要素は、フィールド定義の形式が PropDefV2 である場合にのみ存在します。 内部型では、対応するユーザー定義フィールドの [**新しいフィールド**] ダイアログ ボックス内の型を次の値のいずれかです。 
    
    |**内部型の名前**|**値**|****新しいフィールド**] ダイアログ ボックス内の対応する型**|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**番号** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |通貨型 (Currency)  <br/> |3  <br/> |**通貨型** <br/> |
    |iTypeBool  <br/> |4  <br/> |**はい/いいえ** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**日付/時刻** <br/> |
    |iTypeDuration  <br/> |6  <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7  <br/> |**組み合わせ**、**組み合わせ数式フィールド**] ダイアログ ボックスで選択されている**最初の空ではないフィールドだけ、うちの表示**オプションを使用しています。  <br/> |
    |iTypeFormula  <br/> |8  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9  <br/> |このタイプはユーザー定義フィールドは使用されません。  <br/> |
    |iTypeVariant  <br/> |10  <br/> |このタイプはユーザー定義フィールドは使用されません。  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |このタイプはユーザー定義フィールドは使用されません。  <br/> |
    |iTypeConcat  <br/> |12  <br/> |**組み合わせ**、**参加中のフィールドすべてを相互に****組み合わせ数式フィールド**] ダイアログ ボックスで選択したオプションを使用しています。  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**キーワード** <br/> |
    |iTypeInteger  <br/> |14  <br/> |**Integer** <br/> |
   
- SkipBlocks: [SkipBlock](skipblock-stream-structure.md)ストリームの構造を 1 つまたは複数のデータ系列です。 このデータ要素は、フィールド定義の形式が PropDefV2 である場合にのみ存在します。 フィールド定義の形式が PropDefV2 の場合は、系列を少なくとも 1 つの SkipBlock 構造を 0 に等しいサイズのデータ要素を持つ SkipBlock 構造体を含める必要があり、シリーズが開始し、この構造で SkipBlock を終了する必要があります。 
    
   SkipBlock 構造体の目的は、SkipBlocks シリーズでの相対的な位置に依存します。 フィールド定義は、PropDefV2 の形式で、最初の構造は、(サイズのデータ要素が 0 より大きい) の終端構造ではない場合、Outlook では、最初の SkipBlock 構造体は、Unicode (utf-16) でフィールド名を指定と見なされます。 
    
   > [!IMPORTANT]
   > 最初の SkipBlock では、終端の構造は、フィールド名を確認するのには NameANSI のデータ要素が使用されます。 その文字列には、すべての非 ASCII 文字が含まれている場合、これらの文字が Outlook を実行しているコンピューターの ANSI コード ページによって一貫性がない解釈可能性があります。 このような不整合を防ぐために、フィールド定義を作成することで常に最初の SkipBlock を指定することを確認するには、少なくともとフィールド名が含まれています ASCII 以外の文字には。 
  
   終端の SkipBlock 構造体の前に SkipBlocks シリーズの他の SkipBlock ストリームの構造体としてこのデータを格納できる場合は、フィールド定義の形式の将来のバージョンは、FieldDefinition ストリーム内のデータの追加情報を紹介、サイズのデータ要素が 0 です。 Outlook の以前のバージョンでは、終端の SkipBlock 構造体にこれらの余分な SkipBlock 構造を無視でき、正しくサポートしているすべてのブロックを処理することができます。
    
## <a name="see-also"></a>関連項目

- [Outlook アイテムおよびフィールド](outlook-items-and-fields.md)
- [ストリームの構造](stream-structures.md)
- [PropertyDefinition ストリームの構造](propertydefinition-stream-structure.md)

