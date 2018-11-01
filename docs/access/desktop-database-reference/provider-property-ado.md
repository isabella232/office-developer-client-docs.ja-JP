---
title: Provider プロパティ (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df764aca267cab9b38760c432cd19154d6c6827f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881567"
---
# <a name="provider-property-ado"></a><span data-ttu-id="ce8dd-102">Provider プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ce8dd-102">Provider property (ADO)</span></span>


<span data-ttu-id="ce8dd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ce8dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce8dd-104">[Connection](connection-object-ado.md) オブジェクトのプロバイダー名を示します。</span><span class="sxs-lookup"><span data-stu-id="ce8dd-104">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ce8dd-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="ce8dd-105">Settings and return values</span></span>

<span data-ttu-id="ce8dd-106">プロバイダー名を示す文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce8dd-106">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce8dd-107">解説</span><span class="sxs-lookup"><span data-stu-id="ce8dd-107">Remarks</span></span>

<span data-ttu-id="ce8dd-p101">接続用のプロバイダーの名前を設定または取得するには、**Provider** プロパティを使用します。このプロパティは、[ConnectionString](connectionstring-property-ado.md) プロパティまたは [Open](open-method-ado-connection.md) メソッドの *ConnectionString* 引数の内容によって設定することもできます。ただし、**Open** メソッドを呼び出すときに複数の箇所でプロバイダーを指定すると、予期しない結果が生じる可能性があります。プロバイダーを指定しない場合、このプロパティは既定値の MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)) になります。</span><span class="sxs-lookup"><span data-stu-id="ce8dd-p101">Use the **Provider** property to set or return the name of the provider for a connection. This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results. If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="ce8dd-p102">**Provider** プロパティは、接続が閉じているときは値の設定および取得が可能で、接続が開いているときは値の取得のみが可能です。設定値は **Connection** オブジェクトを開くか、 [Connection](properties-collection-ado.md) オブジェクトの **Properties** コレクションにアクセスするまで有効になりません。設定が無効である場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ce8dd-p102">The **Provider** property is read/write when the connection is closed and read-only when it is open. The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object. If the setting is not valid, an error occurs.</span></span>

