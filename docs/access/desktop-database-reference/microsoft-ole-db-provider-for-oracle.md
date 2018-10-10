---
title: Microsoft OLE DB Provider for Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b4a8847dd7c96813cec6bd8a9868bc9a92b0d2a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477957"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="036ac-102">Microsoft OLE DB Provider for Oracle</span><span class="sxs-lookup"><span data-stu-id="036ac-102">Microsoft OLE DB Provider for Oracle</span></span>

<span data-ttu-id="036ac-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="036ac-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="036ac-104">Microsoft OLE DB Provider for Oracle を使用すると、ADO から Oracle データベースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="036ac-104">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="036ac-105">接続文字列のパラメーター</span><span class="sxs-lookup"><span data-stu-id="036ac-105">Connection String Parameters</span></span>

<span data-ttu-id="036ac-106">このプロバイダーに接続するには、*ConnectionString* プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="036ac-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAORA 
```

<span data-ttu-id="036ac-107">[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="036ac-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

<span data-ttu-id="036ac-p101">キーセットまたは動的カーソル による結合クエリを Oracle データベースで実行すると、エラーが発生します。Oracle では、読み取り専用の静的カーソルのみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="036ac-p101">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs. Oracle only supports a static read-only cursor.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="036ac-110">標準的な接続文字列</span><span class="sxs-lookup"><span data-stu-id="036ac-110">Typical Connection String</span></span>

<span data-ttu-id="036ac-111">このプロバイダーの標準的な接続文字列を次に示します。</span><span class="sxs-lookup"><span data-stu-id="036ac-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

<span data-ttu-id="036ac-112">この文字列は、次に示すキーワードで構成されています。</span><span class="sxs-lookup"><span data-stu-id="036ac-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="036ac-113">キーワード</span><span class="sxs-lookup"><span data-stu-id="036ac-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="036ac-114">説明</span><span class="sxs-lookup"><span data-stu-id="036ac-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="036ac-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-116">OLE DB Provider for Oracle を指定します。</span><span class="sxs-lookup"><span data-stu-id="036ac-116">Specifies the OLE DB Provider for Oracle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036ac-117"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-117"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-118">サーバー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="036ac-118">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="036ac-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-120">ユーザー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="036ac-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036ac-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-122">ユーザー パスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="036ac-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="036ac-123">プロバイダー固有の接続パラメーター</span><span class="sxs-lookup"><span data-stu-id="036ac-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="036ac-p102">このプロバイダーは、ADO で定義されたパラメーターに加えて、プロバイダー固有の接続パラメーターをサポートしています。ADO の接続パラメーターと同様に、これらのプロバイダー固有のプロパティは [Connection](properties-collection-ado.md) の [Properties](connection-object-ado.md) コレクションで設定することも、 **ConnectionString** の一部として設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="036ac-p102">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or as part of the **ConnectionString**.</span></span>

<span data-ttu-id="036ac-p103">これらのパラメーターの詳細については、「OLE DB プログラマ リファレンス」を参照してください。「[ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」では、これらのパラメーターと対応する OLE DB プロパティを相互に参照できます。</span><span class="sxs-lookup"><span data-stu-id="036ac-p103">These parameters are fully described in the OLE DB Programmer's Reference. (The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="036ac-128">パラメーター</span><span class="sxs-lookup"><span data-stu-id="036ac-128">Parameter</span></span></p></th>
<th><p><span data-ttu-id="036ac-129">説明</span><span class="sxs-lookup"><span data-stu-id="036ac-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="036ac-130"><strong>Window Handle</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-130"><strong>Window Handle</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-131">追加情報の入力を求めるために使用するウィンドウ ハンドルを示します。</span><span class="sxs-lookup"><span data-stu-id="036ac-131">Indicates the window handle to use to prompt for additional information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036ac-132"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-132"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-p104">ユーザーの言語に関する設定を指定する一意の 32 ビット番号 (1033 など) を示します。これらの設定は、日付と時刻の形式、アルファベット順の並べ替え方法、文字列の比較方法などを示します。</span><span class="sxs-lookup"><span data-stu-id="036ac-p104">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="036ac-135"><strong>OLE DB Services</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-135"><strong>OLE DB Services</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-136">OLE DB サービスを有効にするか無効にするかを指定するビットマスクを示します。</span><span class="sxs-lookup"><span data-stu-id="036ac-136">Indicates a bitmask that specifies OLE DB services to enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036ac-137"><strong>Prompt</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-137"><strong>Prompt</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-138">接続の確立中にユーザーに入力を求めるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="036ac-138">Indicates whether to prompt the user while a connection is being established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="036ac-139"><strong>Extended Properties</strong></span><span class="sxs-lookup"><span data-stu-id="036ac-139"><strong>Extended Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="036ac-p105">プロバイダー固有の拡張接続情報を含む文字列です。通常のプロパティでは記述できないプロバイダー固有の接続情報についてのみ、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="036ac-p105">A string containing provider-specific, extended connection information. Use this property only for provider-specific connection information that cannot be described through the property mechanism.</span></span></p></td>
</tr>
</tbody>
</table>

