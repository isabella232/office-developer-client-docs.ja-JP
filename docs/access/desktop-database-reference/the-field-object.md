---
title: Field オブジェクト (Access デスクトップ データベースリファレンス)
TOCTitle: The Field object
ms:assetid: 55531e04-d74f-6394-df64-1660e5d572ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249284(v=office.15)
ms:contentKeyID: 48544926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 23b6db5cc5cb64ae0d302f147fcfa0f068338504
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564800"
---
# <a name="field-object"></a>Field オブジェクト

**適用先:** Access 2013、Office 2013

各 **Field** オブジェクトは、通常、データベース テーブル内の列に対応しています。ただし、 **Field** では、チャプターと呼ばれる他の **Recordset** へのポインターを表すこともできます。チャプター列などの例外については、このガイドの後半で説明します。

**Field** オブジェクトの **Value** プロパティを使用すると、カレント レコードのデータを設定または返すことができます。プロバイダーが公開している機能によっては、 **Field** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。

**Field** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。

- **Name** プロパティを使用して、フィールドの名前を返すことができます。

- **Value** プロパティを使用して、フィールド内のデータを表示または変更できます。 **Value** は、 **Field** オブジェクトの既定のプロパティです。

- **Type** 、 **Precision** 、および **NumericScale** の各プロパティを使用して、フィールドの基本的な特性を返すことができます。

- **DefinedSize** プロパティを使用して、フィールドの宣言されたサイズを返すことができます。

- **ActualSize** プロパティを使用して、特定のフィールドに含まれるデータの実際のサイズを返すことができます。

- **Attributes** プロパティおよび **Properties** コレクションを使用して、特定のフィールドについてサポートされている機能の種類を確認できます。

- **AppendChunk** メソッドおよび **GetChunk** メソッドを使用して、長いバイナリ データまたは長い文字データを含むフィールドの値を操作できます。

- プロバイダーがバッチ更新をサポートしている場合は、 **OriginalValue** プロパティおよび **UnderlyingValue** プロパティを使用して、バッチ更新中に発生するフィールドの値の不一致を解決できます。

## <a name="describing-a-field"></a>フィールドの説明

以降のトピックでは、[Field](field-object-ado.md) オブジェクト自体に関する情報、つまりフィールドのメタデータを表す **Field** オブジェクトのプロパティについて説明します。この情報を使用すると、 **Recordset** のスキーマについて多くのことを確認できます。これらのプロパティには、 **Type** 、 **DefinedSize** と **ActualSize** 、 **Name** 、 **NumericScale** と **Precision** などがあります。

## <a name="discovering-the-data-type"></a>データ型の検出

The **Type** property indicates the data type of the field. ADO でサポートされるデータ型列挙定数については、ADO プログラマリファレンスの [DataTypeEnum](datatypeenum.md) *で説明されています*。

**adNumeric** などの浮動小数点型については、より多くの情報を取得できます。 **NumericScale** プロパティは、 **Field** の値を表現するために使用する小数部の桁数を示します。 **Precision** プロパティは、 **Field** の値を表現するために使用する最大桁数を指定します。

## <a name="determining-field-size"></a>フィールド サイズの決定

**DefinedSize** プロパティを使用すると、 **Field** オブジェクトのデータ容量を確認できます。

**ActualSize** プロパティを使用すると、 **Field** オブジェクトの値の実際の長さを返すことができます。 **ActualSize** プロパティは、すべてのフィールドについて読み取り専用です。ADO によって **Field** オブジェクトの値の長さが特定できない場合、 **ActualSize** プロパティは **adUnknown** を返します。

**DefinedSize** プロパティと **ActualSize** プロパティの目的は異なります。たとえば、宣言された型が **adVarChar** で、 **DefinedSize** プロパティの値が 50 である **Field** オブジェクトに、文字が 1 つだけ含まれているとします。この場合、返される **ActualSize** プロパティの値は、この 1 文字のバイト単位の長さとなります。

## <a name="determining-field-contents"></a>フィールドの内容の決定

データ ソースから取得された列の識別子は、 **Field** の **Name** プロパティで表されます。 **Field** オブジェクトの **Value** プロパティは、フィールドの実際の値を返したり、設定したりするために使用します。これは既定のプロパティです。

フィールドの値を変更するには、 **Value** プロパティを適切な型の新しい値に設定します。フィールドの内容を変更するためには、使用しているカーソルが更新をサポートしている必要があります。バッチ モードでは、この時点でデータベースの検証が行われないため、 **UpdateBatch** を呼び出すときにエラーがないことを確認する必要があります。一部のプロバイダーは、ADO **Field** オブジェクトの **UnderlyingValue** プロパティと **OriginalValue** プロパティをサポートしており、バッチ更新を実行しようとしたときに発生する競合の解決に役立ちます。そのような競合の解決方法の詳細については、「 [4 章: データを編集する](chapter-4-editing-data.md)」を参照してください。

> [!NOTE]
> [!メモ] 新しい **Field** を **Recordset** に追加する場合は、 **Recordset Field** の値を設定できません。新しい **Field** は、閉じている **Recordset** に追加できます。追加した後に **Recordset** を開いて、これらの新しい **Field** に値を割り当てる必要があります。

## <a name="getting-more-field-information"></a>フィールド情報の取得

ADO オブジェクトには、組み込みのプロパティと動的プロパティという 2 種類のプロパティがあります。これまでは、 **Field** オブジェクトの組み込みのプロパティについてのみ説明してきました。

組み込みプロパティは、ADO に実装され、構文を使用して新しいオブジェクトですぐに使用できるプロパティです。 これらのプロパティは、オブジェクトの **Properties** コレクションに **Property** オブジェクトとして格納されません。

動的プロパティは、基になるデータ プロバイダーによって定義され、該当する ADO オブジェクトの **Properties** コレクションに含まれます。 たとえば、プロバイダー固有のプロパティには、 **Recordset** オブジェクトがトランザクションや更新をサポートしているかどうかを示すものがあります。 これらの追加のプロパティは、その **Recordset** オブジェクトの **Properties** コレクションに、 **Property** オブジェクトとして格納されます。 動的プロパティは、MyObject.Properties(0) または MyObject.Properties("Name") という構文を使用して、コレクションを通じてのみ参照できます。

どちらの種類のプロパティも削除できません。

動的プロパティである **Property** オブジェクトには、それ自体に次の 4 つの組み込みのプロパティがあります。

- **Name** プロパティは、プロパティを識別する文字列です。

- **Type** プロパティは、プロパティのデータ型を指定する整数です。

- **Value** プロパティは、プロパティの設定を格納する変数です。 **Value** は、 **Property** オブジェクトの既定のプロパティです。

- **Attributes** プロパティは、プロバイダー固有のプロパティの特性を示すロング型 ( **Long** ) の値です。

**Field** オブジェクトの **Properties** コレクションには、フィールドに関する追加のメタデータが含まれます。このコレクションの内容は、プロバイダーによって異なります。この章の最初で使用したサンプルの **Recordset** の **Properties** コレクションを確認するコード例を次に示します。ここでは、まずコレクションの内容を確認します。このコードでは、 [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) を使用しているため、 **Properties** コレクションには、そのプロバイダーに関する情報が格納されています。

```vb 
 
'BeginFieldProps 
 Dim objProp As ADODB.Property 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 
 For Each objProp In objFields(intLoop).Properties 
 Debug.Print vbTab & objProp.Name & " = " & objProp.Value 
 Next objProp 
 Next intLoop 
'EndFieldProps 
```

## <a name="dealing-with-binary-data"></a>バイナリ データの処理

[Field](appendchunk-method-ado.md) オブジェクトの **AppendChunk** メソッドを使用すると、そのオブジェクトに長いバイナリ データまたは文字データを格納できます。システムのメモリ容量が少ない場合、 **AppendChunk** メソッドを使用して、長い値の全体ではなく一部を操作できます。

**Field** オブジェクトの **Attributes** プロパティの **adFldLong** ビットが **True** に設定されている場合は、そのフィールドに対して **AppendChunk** メソッドを使用できます。

**Field** オブジェクトで最初に **AppendChunk** を呼び出すと、フィールドにデータが書き込まれますが、既存のデータは上書きされます。それ以降に **AppendChunk** を呼び出すと、既存のデータに追加されます。あるフィールドにデータを追加した後に、カレント レコードに含まれる他のフィールドの値を設定したり読み込んだりすると、ADO は、最初のフィールドに対するデータの追加操作が完了したものと見なします。最初のフィールドに対して再度 **AppendChunk** メソッドを呼び出すと、ADO はその呼び出しを新しい **AppendChunk** 操作として仲介し、既存のデータを上書きします。一方、最初の **Recordset** オブジェクトの複製でない他の **Recordset** オブジェクトのフィールドにアクセスしても、 **AppendChunk** 操作は中断されません。

**Field** オブジェクトの **GetChunk** メソッドを使用すると、長いバイナリ データまたは文字データの一部または全体を取得できます。システムのメモリ容量が少ない場合、 **GetChunk** メソッドを使用して、長い値の全体ではなく一部を操作できます。

**GetChunk** への呼び出しによって返される値は、*variable* に格納されます。*Size* が残りのデータよりも大きい場合、**GetChunk** メソッドは、*variable* の余った部分を空白で埋めることはなく、残りのデータのみを返します。フィールドが空の場合、**GetChunk** メソッドは Null 値を返します。

**GetChunk** を連続して呼び出すと、直前の **GetChunk** の呼び出しで取得されたデータの直後からデータが取得されます。ただし、あるフィールドのデータを取得しているときに、カレント レコードの別のフィールドの値の設定または読み取りを行うと、ADO は、最初のフィールドからのデータ取得は終了したと見なします。最初のフィールドでもう一度 **GetChunk** メソッドを呼び出すと、ADO は、その呼び出しを新しい **GetChunk** 操作と解釈し、データの先頭から読み取りを開始します。最初の **Recordset** オブジェクトの複製を除く別の **Recordset** オブジェクトのフィールドにアクセスした場合、 **GetChunk** 操作は中断されません。

**Field** オブジェクトの **Attributes** プロパティの **adFldLong** ビットが **True** に設定されている場合は、そのフィールドに対して **GetChunk** メソッドを使用できます。

**Field** オブジェクトの **GetChunk** メソッドまたは **AppendChunk** メソッドを使用したときに、カレント レコードが存在しない場合は、エラー 3021 (カレント レコードがありません) が発生します。

これらのメソッドを使用してバイナリ データを操作する例については *、ADO* プログラマリファレンスの [AppendChunk メソッド](appendchunk-method-ado.md)と [GetChunk メソッド](getchunk-method-ado.md)の例を参照してください。

