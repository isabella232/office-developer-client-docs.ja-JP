---
title: サポートされている内容を確認する
TOCTitle: Determining What is Supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6114dd0fa56a87b6c2e07770795ea5889ae3c44
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883632"
---
# <a name="determining-what-is-supported"></a><span data-ttu-id="742bc-102">サポートされている内容を確認する</span><span class="sxs-lookup"><span data-stu-id="742bc-102">Determining What is Supported</span></span>


<span data-ttu-id="742bc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="742bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="742bc-p101">**Supports** メソッドは、指定された **Recordset** オブジェクトが、特定の種類の機能をサポートしているかどうかを確認するために使用します。構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="742bc-p101">The **Supports** method is used to determine whether a specified **Recordset** object supports a particular type of functionality. It has the following syntax:</span></span>

`boolean = recordset.Supports( CursorOptions )`

<span data-ttu-id="742bc-p102">**Supports** は、*CursorOptions* 引数で指定されているすべての機能が、プロバイダーによってサポートされているかどうかを示すブール値を返します。**Supports** メソッドを使用すると、**Recordset** オブジェクトがどのような種類の機能をサポートしているのかを確認できます。*CursorOptions* で対応する定数が指定されている機能を、**Recordset** オブジェクトがサポートしている場合、**Supports** メソッドは **True** を返します。それ以外の場合は、**False** を返します。</span><span class="sxs-lookup"><span data-stu-id="742bc-p102">**Supports** returns a Boolean value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider. You can use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>

<span data-ttu-id="742bc-p103">**Supports** メソッドを使用すると、 **Recordset** オブジェクトが、新しいレコードの追加、ブックマークの使用、 **Find** メソッドの使用、スクロールの使用、 **Index** プロパティの使用、およびバッチ更新の実行に対応できるかどうかを確認できます。定数とその意味をすべて記載した一覧については、「 [CursorOptionEnum](cursoroptionenum.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="742bc-p103">Using the **Supports** method, you can check for the ability of the **Recordset** object to add new records, use bookmarks, use the **Find** method, use scrolling, use the **Index** property, and to perform batch updates. For a complete list of constants and their meanings, see [CursorOptionEnum](cursoroptionenum.md).</span></span>

<span data-ttu-id="742bc-p104">**Supports** メソッドが特定の機能について **True** を返す場合でも、プロバイダーがすべての状況でその機能を実現できるとは限りません。 **Supports** メソッドは、特定の条件が満たされているという仮定の下で、プロバイダーが指定された機能をサポートできるかどうかを返すに過ぎません。たとえば、カーソルで複数テーブルの結合が想定されている場合は一部の列を更新できませんが、 **Supports** メソッドでは **Recordset** オブジェクトが更新をサポートしていると示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="742bc-p104">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates, even though the cursor is based on a multiple table join — some columns of which are not updateable.</span></span>

