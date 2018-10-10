---
title: Prepared プロパティ (ADO)
TOCTitle: Prepared Property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 865453f89cd5942ec7f9f8d036beb72dc519397e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476492"
---
# <a name="prepared-property-ado"></a><span data-ttu-id="2fcc3-102">Prepared プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="2fcc3-102">Prepared Property (ADO)</span></span>


<span data-ttu-id="2fcc3-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fcc3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2fcc3-104">コンパイルされたバージョンのコマンドを実行前に保存するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2fcc3-104">Indicates whether to save a compiled version of a command before execution.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2fcc3-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="2fcc3-105">Settings and Return Values</span></span>

<span data-ttu-id="2fcc3-106">ブール型 ( **Boolean** ) の値を設定または取得します。 **True** に設定されている場合は、コマンドの準備が必要であることを示します。</span><span class="sxs-lookup"><span data-stu-id="2fcc3-106">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fcc3-107">解説</span><span class="sxs-lookup"><span data-stu-id="2fcc3-107">Remarks</span></span>

<span data-ttu-id="2fcc3-p101">**Command** オブジェクトを最初に実行する前に、 [CommandText](commandtext-property-ado.md) プロパティで指定されたクエリの準備済み (コンパイル済み) バージョンをプロバイダーで保存するには、 [Prepared](command-object-ado.md) プロパティを使用します。これによって、コマンドの最初の実行は遅くなることがありますが、プロバイダーでコマンドをコンパイルした後はコンパイル済みのコマンドが使用されるので、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="2fcc3-p101">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution. This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="2fcc3-110">このプロパティが **False** の場合、プロバイダーはコンパイル済みバージョンを作成せずに、直接 **Command** オブジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="2fcc3-110">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="2fcc3-p102">プロバイダーがコマンドの準備をサポートしていない場合、このプロパティを **True** に設定すると、すぐにエラーが返されることがあります。エラーを返さない場合、プロバイダーは単にコマンドの準備の要求を無視し、 **Prepared** プロパティを **False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2fcc3-p102">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**. If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

