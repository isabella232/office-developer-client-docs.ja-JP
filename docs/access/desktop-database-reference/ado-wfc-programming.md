---
title: ADO/WFC プログラミング
TOCTitle: ADO/WFC Programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea531f484ad75de268f0d4fb38a10e617c1851e6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884633"
---
# <a name="adowfc-programming"></a><span data-ttu-id="53016-102">ADO/WFC プログラミング</span><span class="sxs-lookup"><span data-stu-id="53016-102">ADO/WFC Programming</span></span>


<span data-ttu-id="53016-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="53016-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53016-p101">Microsoft Visual J++ 6.0 の場合、Windows Foundation Classes (WFC) と共に機能するように ADO が次のように拡張されました。まず、Java クラス セットの実装により ADO インターフェイスが拡張され、Java プログラマに役立つ通知が追加されました。また、Java クラスでは、Java 型をユーザーに返す関数も提供されます。パフォーマンスを向上させるため、Java クラスは、OLE DB 行セット オブジェクトのネイティブ データ型に直接アクセスし、バリアント型 (Variant) への変換やバリアント型からの変換を行わずに Java 型として Java プログラマに返します。また、ADO は、WFC フレームワークのイベント通知でも機能するように拡張されました。</span><span class="sxs-lookup"><span data-stu-id="53016-p101">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways. First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user. To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant. ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="53016-p102">Windows Foundation Classes 用の ADO (ADO/WFC) は、標準の ADO のメソッド、プロパティ、オブジェクト、およびイベントをすべてサポートしています。ただし、パラメーターとしてバリアント型 (variant) を必要とし、Microsoft Visual Basic などの言語で高いパフォーマンスを示すような操作を、Visual J++ などの言語で実行するとパフォーマンスが低下します。そのため、ADO/WFC では、[Field](field-object-ado.md) オブジェクトで、バリアント型のデータではなくネイティブな Java データ型を使用するアクセス機能を用意しています。</span><span class="sxs-lookup"><span data-stu-id="53016-p102">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events. However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++. For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="53016-111">ADO/WFC パッケージの詳細については、ADO のマニュアルの「[ADO/WFC 構文インデックス](https://msdn.microsoft.com/library/jj250066\(v=office.15\))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53016-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="53016-112">ライブラリの参照</span><span class="sxs-lookup"><span data-stu-id="53016-112">Referencing the Library</span></span>

<span data-ttu-id="53016-113">ADO/WFC データ クラスをプロジェクトにインポートするには、次の行をコードに追加します。</span><span class="sxs-lookup"><span data-stu-id="53016-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```

