---
title: FieldDefinition ストリーム構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2277d66a4f46a64f6e5fce9cad747fb98e767701
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588036"
---
# <a name="fielddefinition-stream-structure"></a>FieldDefinition ストリーム構造

**適用対象**: Outlook 2013 | Outlook 2016 
  
FieldDefinition ストリーム構造には、ユーザー定義フィールドのフィールド定義、または組み込みフィールドのデータ バインド設定のセットが含まれます。
  
ユーザー定義フィールドのフィールド定義が構造体に含まれている場合は、プログラムによって FieldDefinition ストリーム構造を操作できます。 組み込みフィールドの設定が構造体に含まれている場合は、プログラムによって FieldDefinition 構造を作成または変更しようとはしません。 Microsoft Outlook フォーム デザイナーを使用して、組み込みフィールドの設定を維持する必要があります。
  
> [!NOTE]
> Outlookは、PropDefV1 と PropDefV2 の 2 つの形式のフィールド定義をサポートしています。 フィールド定義の PropDefV1 形式には、Flags、VT、DispId、NmidNameLength、NmidName、NameANSI、FormulaANSI、ValidationRuleANSI、ValidationTextANSI、ErrorANSI のデータ要素が含まれます。 PropDefV2 形式には、同じ要素と InternalType 要素と SkipBlocks 要素が含まれます。 
>
> Outlook PropDefV2 フィールド定義形式の FormulaANSI、ValidationRuleANSI、ValidationTextANSI データ要素の Unicode バージョンは維持しません。 これらの要素に ASCII 以外の文字が含まれている場合、これらの文字は、コンピューターで実行されている ANSI コード ページに応じて一貫性Outlookがあります。 したがって、これらのデータ要素には、ASCII 文字で完全に構成される文字列値のみを使用する必要があります。 
  
このストリーム内のデータ要素は、リトル エンディアン バイト順に格納され、次に示す順序で互いに直後に格納されます。
  
- フラグ: DWORD (4 バイト)、0 個以上のフラグの組み合わせで、値と意味を次の表に示します。
    
    |**フラグ名**|**値**|**説明**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |FieldDefinition 構造体には、ユーザー定義フィールドの定義が含まれる。  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |このフィールドにバインドされているフォーム コントロールの場合、このフィールドの **値** のチェック ボックスが [プロパティ]ダイアログ ボックスの [検証] タブ **で** 選択されている必要があります。  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |このフィールドにバインドされたフォーム コントロールの場合、[プロパティ]ダイアログ ボックスの [検証] タブで、[印刷にこのフィールドを含める] チェック ボックスと [名前を付けて保存] のチェック ボックス **が** オンです。  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |このフィールドにバインドされているフォーム コントロールの場合、[プロパティ]ダイアログ ボックスの [値]タブで、[この数式を自動的に計算する] チェック ボックス **が** オンになります。  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |これは、Combination 型のフィールドであり、[結合フィールド] と [結合式フィールド] ダイアログ ボックスで選択されている他のオプションを持つ任意のテキスト フラグメント **を持っています**。  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |このフィールドは Combination 型で、[組み合わせ数式フィールド] ダイアログ ボックスで選択されている後続のフィールドを無視して、最初の空でないフィールドのみを表示します。   <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |このフラグは、ユーザー定義Outlook使用されるのではなく、すべてのユーザー定義フィールド定義に含まれます。  <br/> |
   
- VT: WORD (2 バイト)、フィールドのデータ型 [(VARENUM](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) 列挙からの定数)。 
    
- DispId: DWORD (4 バイト)、フィールドのディスパッチ識別子。 ユーザー定義フィールドの場合、値は 0 です。
    
- NmidNameLength: WORD (2 バイト)、NmidName 配列内の要素の数。
    
- NmidName: WCHAR の配列。 ユーザー定義フィールド定義の場合、これはフィールド名の Unicode (UTF-16) 表記です。 この配列の数は NmidNameLength と等しくなります。
    
- NameANSI: [PackedAnsiString ストリーム](packedansistring-stream-structure.md) 構造。 これは、フィールド名の ANSI 表記です。 
    
- FormulaANSI: PackedAnsiString ストリーム構造。 これは、フィールドの数式の ANSI 表現です。 このフィールドにバインドされたフォーム コントロール **の**  [プロパティ]ダイアログ ボックスの [値] タブの [初期値] セクションに表示されます。 
    
- ValidationRuleANSI: PackedAnsiString ストリーム構造。 これは、フィールドの検証式の ANSI 表現です。 このフィールドにバインドされているフォーム コントロールの [プロパティ] ダイアログボックスの [検証] タブにある [検証式] のテキスト ボックスに表示されます。  
    
- ValidationTextANSI: PackedAnsiString ストリーム構造。 これは、フィールドの検証エラー テキストの ANSI 表現です。 このフィールドにバインドされているフォーム コントロールの [プロパティ] ダイアログ ボックスの [検証] タブで検証が失敗した場合は、[このメッセージを表示する] のテキスト ボックスに表示されます。  
    
- ErrorANSI: PackedAnsiString ストリーム構造。 Outlookこの要素は使用しない。この要素を空の文字列に設定する必要があります。
    
- InternalType: DWORD (4 バイト)、フィールドの内部型。 このデータ要素は、フィールド定義形式が PropDefV2 の場合にのみ存在します。 内部型は、ユーザー定義フィールドの [新しいフィールド] ダイアログ ボックスの型に対応する、次のいずれかの値です。 
    
    |**内部型名**|**値**|**[新しいフィールド] **ダイアログ ボックスの対応** する型**|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**数値** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |通貨  <br/> |3  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4   <br/> |**はい/いいえ** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**日付/時刻** <br/> |
    |iTypeDuration  <br/> |6   <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7   <br/> |**[** 組み合 **わせ]** 、 [組み合わせ数式フィールド] ダイアログ ボックスで選択されている後続のフィールドを無視して、最初の空でないフィールドのみを表示 **する** オプションを指定します。  <br/> |
    |iTypeFormula  <br/> |8   <br/> |**式** <br/> |
    |iTypeResult  <br/> |9   <br/> |この型は、ユーザー定義フィールドには使用されません。  <br/> |
    |iTypeVariant  <br/> |10  <br/> |この型は、ユーザー定義フィールドには使用されません。  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |この型は、ユーザー定義フィールドには使用されません。  <br/> |
    |iTypeConcat  <br/> |12   <br/> |**[** 結合フィールド] と [結合フィールド] **および [** 組み合わせ数式フィールド] ダイアログ ボックスで選択されている任意のテキスト **フラグメント** を組み合わせて指定します。  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**キーワード** <br/> |
    |iTypeInteger  <br/> |14   <br/> |**Integer** <br/> |
   
- SkipBlocks: 一連の 1 つ以上の [SkipBlock ストリーム](skipblock-stream-structure.md) 構造。 このデータ要素は、フィールド定義形式が PropDefV2 の場合にのみ存在します。 フィールド定義の形式が PropDefV2 の場合、系列には少なくとも 1 つの SkipBlock 構造体、Size データ要素が 0 の SkipBlock 構造体が含まれている必要があります。この SkipBlock 構造体で系列を開始および終了する必要があります。 
    
   SkipBlock 構造体の目的は、SkipBlocks シリーズの相対位置によって異なります。 フィールド定義が PropDefV2 形式で、最初の構造体が終了構造ではない場合 (Size データ要素が 0 より大きい) 場合、Outlook は最初の SkipBlock 構造体が Unicode (UTF-16) でフィールド名を指定すると仮定します。 
    
   > [!IMPORTANT]
   > 最初の SkipBlock が終了構造の場合、NameANSI データ要素を使用してフィールド名を決定します。 その文字列に ASCII 以外の文字が含まれている場合、これらの文字は、その文字列が実行されているコンピューターの ANSI コード ページに応じて一貫性Outlookがあります。 このような不整合を防ぐには、少なくともフィールド名に ASCII 以外の文字が含まれている場合は、作成するフィールド定義で最初の SkipBlock を必ず指定してください。 
  
   将来のバージョンのフィールド定義形式で FieldDefinition ストリームに追加のデータが含まれる場合、このデータは、Size データ要素が 0 に等しい終了する SkipBlock 構造体の前に、SkipBlocks シリーズに追加の SkipBlock ストリーム構造として格納できます。 以前のバージョンOutlook、これらの余分な SkipBlock 構造体を終了する SkipBlock 構造体まで無視して、サポートしているすべてのブロックを正しく処理できます。
    
## <a name="see-also"></a>関連項目

- [Outlookアイテムとフィールド](outlook-items-and-fields.md)
- [Stream 構造](stream-structures.md)
- [PropertyDefinition ストリーム構造](propertydefinition-stream-structure.md)

