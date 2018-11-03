---
title: ADO/WFC プログラミング
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58ec04f92bf4d1eaaa8ea36c5937cae0bab3729f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943823"
---
# <a name="adowfc-programming"></a><span data-ttu-id="abaea-102">ADO/WFC プログラミング</span><span class="sxs-lookup"><span data-stu-id="abaea-102">ADO/WFC programming</span></span>

<span data-ttu-id="abaea-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="abaea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="abaea-p101">Microsoft Visual J++ 6.0 の場合、Windows Foundation Classes (WFC) と共に機能するように ADO が次のように拡張されました。まず、Java クラス セットの実装により ADO インターフェイスが拡張され、Java プログラマに役立つ通知が追加されました。また、Java クラスでは、Java 型をユーザーに返す関数も提供されます。パフォーマンスを向上させるため、Java クラスは、OLE DB 行セット オブジェクトのネイティブ データ型に直接アクセスし、バリアント型 (Variant) への変換やバリアント型からの変換を行わずに Java 型として Java プログラマに返します。また、ADO は、WFC フレームワークのイベント通知でも機能するように拡張されました。</span><span class="sxs-lookup"><span data-stu-id="abaea-p101">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways. First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user. To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant. ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="abaea-p102">Windows Foundation Classes 用の ADO (ADO/WFC) は、標準の ADO のメソッド、プロパティ、オブジェクト、およびイベントをすべてサポートしています。ただし、パラメーターとしてバリアント型 (variant) を必要とし、Microsoft Visual Basic などの言語で高いパフォーマンスを示すような操作を、Visual J++ などの言語で実行するとパフォーマンスが低下します。そのため、ADO/WFC では、[Field](field-object-ado.md) オブジェクトで、バリアント型のデータではなくネイティブな Java データ型を使用するアクセス機能を用意しています。</span><span class="sxs-lookup"><span data-stu-id="abaea-p102">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events. However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++. For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="abaea-111">ADO/WFC パッケージの詳細については、ADO のマニュアルの「[ADO/WFC 構文インデックス](https://msdn.microsoft.com/library/jj250066\(v=office.15\))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abaea-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="abaea-112">ライブラリを参照します。</span><span class="sxs-lookup"><span data-stu-id="abaea-112">Referencing the library</span></span>

<span data-ttu-id="abaea-113">ADO/WFC データ クラスをプロジェクトにインポートするには、次の行をコードに追加します。</span><span class="sxs-lookup"><span data-stu-id="abaea-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```

