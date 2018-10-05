---
title: フォルダー フィールド ストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385089"
---
# <a name="folder-fields-stream-structures"></a>フォルダー フィールド ストリームの構造

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの[PidTagUserFields](pidtaguserfields-canonical-property.md)プロパティには、バイナリ ストリーム、フォルダーのユーザー定義フィールドの定義が含まれている、FolderUserFields が含まれています。 このトピックでは、フォルダーのユーザー定義フィールドの定義についてはストリームの構造体について説明します。 

FolderUserFields ストリームの構造体は、FolderUserFieldsA 構造体または FolderUserFieldsW 構造体の後に FolderUserFieldsA 構造体のいずれかで構成されます。
  
このストリーム内のデータ要素は、次の指定された順序で互いのすぐ後に格納されています。
  
- **FolderUserFieldsAnsi**: FolderUserFieldsA 構造体をストリーム配信します。
    
- **FolderUserFieldsUnicode**(オプション): FolderUserFieldsW 構造体をストリーム配信します。
    
FolderUserFieldsAnsi の長さ以上である FolderUserFields の長さの合計で FolderUserFieldsUnicode の存在が検出されました。
  
> [!IMPORTANT]
> FolderUserFieldsAnsi が使用される以前、unicode 対応でない、MAPI クライアントのバージョンとの互換性のため FolderUserFieldsUnicode が存在する場合、FolderUserFieldsAnsi の内容は無視されます。 データを避けるために ANSI 変換、常に FolderUserFields ストリームを作成するときに失われるには、FolderUserFieldsW の一部が含まれます。 
  
## <a name="folderuserfieldsa-stream-structure"></a>FolderUserFieldsA ストリームの構造

FolderUserFieldsA ストリームの構造体は、FolderUserFieldsW、FolderUserFields 構造体の一部が上書きされない限り、Outlook フォルダー内のすべてのユーザー定義フィールドの定義を含む FolderFieldDefinitionA ストリームの構造体の配列です。
  
リトル エンディアンのバイト順は、次の指定された順序で互いのすぐ後に、このストリーム内のデータ要素が格納されます。
  
- **FieldDefinitionCount**: DWORD (4 バイト) で、このストリーム内のフィールドの定義の数です。 これは、 **FieldDefinitions**配列の要素の数です。
    
- **FieldDefinitions**: FolderFieldDefinitionA の配列が構造体をストリーム配信します。 この配列は、 **FieldDefinitionCount**のデータ要素と同じです。
    
オーバーライドされない限りこの FolderUserFieldsA は、FolderUserFieldsW、FolderUserFields 構造体の一部で、 **FieldDefinitions**配列する必要があります「null で終わる」の最後の FolderFieldDefinitionA 要素の Common.FieldType フィールドの値のことで、ftNull。
  
## <a name="folderuserfieldsw-stream-structure"></a>FolderUserFieldsW ストリームの構造

FolderUserFieldsW ストリームの構造体は、Outlook フォルダー内のすべてのユーザー定義フィールドの定義を含む FolderFieldDefinitionW ストリームの構造体の配列です。
  
リトル エンディアンのバイト順は、次の指定された順序で互いのすぐ後に、このストリーム内のデータ要素が格納されます。
  
- **FieldDefinitionCount**: DWORD (4 バイト) で、このストリーム内のフィールドの定義の数です。 これは、 **FieldDefinitions**配列の要素の数です。
    
- **FieldDefinitions**: FolderFieldDefinitionW の配列が構造体をストリーム配信します。 この配列は、 **FieldDefinitionCount**のデータ要素と同じです。
    
**FieldDefinitions**配列する必要があります「null で終わる」の最後の FolderFieldDefinitionW 要素の Common.FieldType フィールドを ftNull にすることによって。
  
## <a name="folderfielddefinitiona-stream-structure"></a>FolderFieldDefinitionA ストリームの構造

FolderFieldDefinitionA ストリームの構造体には、ansi 形式で格納されているフィールド名を持つユーザー定義のフィールドの定義が含まれています。
  
リトル エンディアンのバイト順は、次の指定された順序で互いのすぐ後に、このストリーム内のデータ要素が格納されます。
  
- **FieldType**: FldType (4 バイト) で、このフィールドの種類です。
    
- **FieldNameLength**: ワード (2 バイト) で、**フィールド名**の配列内の要素の数。
    
- **フィールド名**: char 型の配列。 つまり、CP_ACP の ANSI コード ページ形式のフィールド名です。 この配列の数は**FieldNameLength**になります。 フィールド名は、 [UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx)メソッドで指定された Name パラメーターの制限を満たす必要があります。 
    
   > [!NOTE]
   > レガシー互換性の理由から、Outlook は**フィールド名**の値がないこれらの制限を満たすいくつか、しかしこのような場合が対応していないこのトピックを処理することにあります。 
  
- **共通**: FolderFieldDefinitionCommon 構造体をストリーム配信します。
    
## <a name="folderfielddefinitionw-stream-structure"></a>FolderFieldDefinitionW ストリームの構造

FolderFieldDefinitionW ストリームの構造体には、Unicode で格納されているフィールド名を持つユーザー定義のフィールドの定義が含まれています。
  
リトル エンディアンのバイト順は、次の指定された順序で互いのすぐ後に、このストリーム内のデータ要素が格納されます。
  
- **FieldType**: FldType (4 バイト) で、このフィールドの種類です。
    
- **FieldNameLength**: ワード (2 バイト) で、**フィールド名**の配列内の要素の数。
    
- **フィールド名**: wchar 型の配列。 これは、Unicode (utf-16) の形式のフィールド名です。 この配列の数は**FieldNameLength**になります。 フィールド名は、 [UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx)メソッドで指定された Name パラメーターの制限を満たす必要があります。 
    
   > [!NOTE]
   > レガシー互換性の理由から、Outlook はしないこれらの制限を満たすいくつかの**フィールド**値を処理できる場合がありますが、このような場合は、このトピックでは説明しません。 
  
- **共通**: FolderFieldDefinitionCommon 構造体をストリーム配信します。
    
## <a name="fldtype-enumeration"></a>FldType 列挙型

**FldType**列挙値は、次の表に表示されます。 
  
|名前|値|意味|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |フィールド定義の配列を null で終了するのには、この種類のフィールドが使用されます。  <br/> |
|ftString  <br/> |0x1  <br/> |テキスト  <br/> |
|ftInteger  <br/> |0x3  <br/> |整数  <br/> |
|ftTime  <br/> |0x5  <br/> |日付/時刻型  <br/> |
|ftBoolean  <br/> |0x6  <br/> |はい/いいえ  <br/> |
|ftDuration  <br/> |0x7  <br/> |Duration  <br/> |
|ftMultiString  <br/> |0 xb  <br/> |Keywords  <br/> |
|ftFloat  <br/> |0xC  <br/> |数値または割合  <br/> |
|ftCurrency  <br/> |0xE  <br/> |通貨型 (Currency)  <br/> |
|ftCalc  <br/> |0x12  <br/> |式  <br/> |
|ftSwitch  <br/> |0x13  <br/> |表示のみ最初空でないフィールドのうちの種類の組み合わせです。  <br/> |
|ftConcat  <br/> |0x17  <br/> |結合するフィールドすべてを他の種類の組み合わせです。  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>FolderFieldDefinitionCommon ストリームの構造

FolderFieldDefinitionCommon ストリームの構造体には、FolderFieldDefinitionA と、FolderFieldDefinitionW の両方に共通するユーザー定義のフィールド定義のデータが含まれています。
  
リトル エンディアンのバイト順は、次の指定された順序で互いのすぐ後に、このストリーム内のデータ要素が格納されます。
  
- **PropSetGuid**: GUID (16 バイト)、プロパティは、フォルダー フィールドの対応する MAPI プロパティ名の GUID を設定します。 このフィールドの値でなければなりません PS_PUBLIC_STRINGS でない限り、フィールドの種類**ftNone**場合にこのフィールドの値が GUID_ 値にする必要があります。 
    
   > [!NOTE]
   > レガシー互換性の理由から、Outlook がされないこの制限を満たすいくつかの**PropSetGuid**値、しかしこのような場合が対応していないこのトピックを処理することがあります。 
  
- **fcapm**: DWORD (4 バイト)、および意味の値が次の表に記載されている 1 つ以上のフラグの組み合わせです。 フラグを同じ値では、フィールドの型、つまり、FldType の値に依存する意味を持っています。
    
    |フラグ名|値|意味|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |フィールドは編集可能です。  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |フィールドは、並べ替えができます。  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |フィールドは、調べたりします。  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |フィールドは、複数行のテキストを保持できます。  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |この型 ftFloat は、割合フィールドです。  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |型 ftTime のこのフィールドは、日付だけの時間フィールドです。  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |型 ftInteger のこのフィールドの単位は許可されませんの表示形式です。としてこのような形式の"コンピューター - 640 の K.."は許可されていません。  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |アイテムでフィールドを編集することができます: これは、具体的にはユーザー設定フォームです。  <br/> |
   
- **dwString**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **dwBitmap**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **dwDisplay**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **iFmt**: INT (4 バイト)。 持つフィールド型に対して、"形式:」ダイアログ ボックスの [新しいフィールドの"、"フィールドの編集]、および [フィールド プロパティ] のコンボ ボックス、コンボ ボックスで選択した形式の 0 から始まるインデックス。 種類のフィールドをコンボ ボックスを使用せずに 0 でなければなりません。 フィールドの種類とフィールドの値が一意に、 **dwString**、 **dwBitmap**の値を決定し、 **dwDisplay**フィールドでは、最初の次の注を参照してください。
    
- **wszFormulaLength**: ワード (2 バイト)、 **wszFormulaLength**配列内の要素の数。
    
- **wszFormulaLength**: wchar 型の配列。 これは、標準の形式でのフィールドの数式文字列の Unicode (utf-16) 形式です。 標準の説明と、フィールドの数式の UI 形式の 2 つ目の次の注を参照してください。 この配列の数は**wszFormulaLength**になります。 数式の文字列は、フィールドの型が**ftCalc**、 **ftSwitch**または**ftConcat**でない限り、空の文字列にすることがあります。
    
> [!NOTE]
> 冗長は、 **FldType**の値と、 **iFmt**の値に基づいて**dwString**、 **dwBitmap**、および**dwDisplay**の値は一意に決まりますが適切な値はまだのために必要な正しいoutlook フィールドの定義の処理をします。 この決定を実行するアルゴリズムの簡単な説明はありません。 
> 
> したがって、どの**dwString**、 **dwBitmap**、および**dwDisplay**値に対応して、指定した**FldType**値と**iFmt**の値を検索] を選択する形式と、その種類のユーザー定義フィールドを作成してテストを実行します。**フォーマット**」コンボ ボックスで、適用できると仮定して、結果として得られる**FolderUserFields**ストリームを対象となるユーザー定義フィールドが作成されますを確認します。 
  
**新しいフィールド**、**フィールドの編集**、およびユーザー定義フィールドの**フィールドのプロパティ**ダイアログ ボックスの [**数式**] テキスト ボックス内の UI 形式でのフィールドの数式を編集します。 UI 形式の数式を標準の形式に変換するアルゴリズムは、次の説明に従ってフィールドの種類によって異なります。 
- タイプ**ftCalc**および**ftSwitch**のフィールドは、組み込みのフィールドは、対応する MAPI プロパティは、標準的な形式という名前のプロパティの種類の MNID\_の文字列はフィールドの名前の一部を置き換えることによって取得されます`[<field_name>]`フラグメントを使用した`[_<field_dispid_decimal>]`。 

  たとえば、**数式**、 **ftCalc**、Office UI 言語が英語 (米国) の中では、型のフィールドの数式は、UI の形式は、 `[Business Phone] & [My custom field]`、`My custom field`名前のユーザー定義のフィールドでは、このような数式の標準の形式になります`[_14856] & [My custom field]`.

- **FtConcat**の型のフィールドは、次を実行して標準の形式を取得します。

  1. 先頭および末尾の空白文字が切り捨てられます。 
  2. 以下の 2 種類のフラグメントのシーケンスには、式を解析します。 
     - フィールド名は角かっこで`[<field_name>]`です。 
     - 角かっこが含まれていない部分です。   
      第二種のない 2 つのフラグメントは、シーケンス内の連続したことを保証します。 場合は、数式には、この方法を解析できない場合、無効と見なされます。 
  3. **FtCalc**と**ftSwitch**フィールドと 1 つのフラグメントの同一の置換を実行します。 
  4. 第二種の各フラグメントのすべての二重引用符をエスケープします (""") 文字、2 つの連続した二重引用符文字である場合、二重引用符で囲みます。 
  5. アンパサンド文字列を挿入 (`&`) 隣接するフラグメントの各ペアの間です。
 
  **FtConcat**の型のフィールドの数式の UI 形式の場合など、Office UI 言語を英語 (米国) を使用して`text1 [Business Phone] "text2" [My custom field]`、`My custom field`標準の書式設定、ユーザー定義フィールドの名前は、このような数式になるの`""text1" & [_14856] & """text2""" & [My custom field]"`。 
  
## <a name="see-also"></a>関連項目

- [FolderUserFields ストリームのサンプル](folderuserfields-stream-sample.md)
- [新しいユーザー定義フィールドの定義を追加する](how-to-add-a-definition-for-a-new-user-defined-field.md)

