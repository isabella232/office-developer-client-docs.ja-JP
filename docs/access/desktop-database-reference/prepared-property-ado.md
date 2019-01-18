---
title: Prepared プロパティ (ADO)
TOCTitle: Prepared property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9541b2d584728c09ee852f628cdfc35f3d170f04
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718071"
---
# <a name="prepared-property-ado"></a><span data-ttu-id="45e26-102">Prepared プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="45e26-102">Prepared property (ADO)</span></span>


<span data-ttu-id="45e26-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="45e26-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45e26-104">コンパイルされたバージョンのコマンドを実行前に保存するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="45e26-104">Indicates whether to save a compiled version of a command before execution.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="45e26-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="45e26-105">Settings and return values</span></span>

<span data-ttu-id="45e26-106">ブール型 ( **Boolean** ) の値を設定または取得します。 **True** に設定されている場合は、コマンドの準備が必要であることを示します。</span><span class="sxs-lookup"><span data-stu-id="45e26-106">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="45e26-107">解説</span><span class="sxs-lookup"><span data-stu-id="45e26-107">Remarks</span></span>

<span data-ttu-id="45e26-p101">**Command** オブジェクトを最初に実行する前に、 [CommandText](commandtext-property-ado.md) プロパティで指定されたクエリの準備済み (コンパイル済み) バージョンをプロバイダーで保存するには、 [Prepared](command-object-ado.md) プロパティを使用します。これによって、コマンドの最初の実行は遅くなることがありますが、プロバイダーでコマンドをコンパイルした後はコンパイル済みのコマンドが使用されるので、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="45e26-p101">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution. This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="45e26-110">このプロパティが **False** の場合、プロバイダーはコンパイル済みバージョンを作成せずに、直接 **Command** オブジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="45e26-110">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="45e26-p102">プロバイダーがコマンドの準備をサポートしていない場合、このプロパティを **True** に設定すると、すぐにエラーが返されることがあります。エラーを返さない場合、プロバイダーは単にコマンドの準備の要求を無視し、 **Prepared** プロパティを **False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="45e26-p102">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**. If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

