---
title: '手順 5: DataControl を利用可能にする (RDS チュートリアル)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e5871138f2b82770f49da2d5f9d4977443b0664e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884045"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a><span data-ttu-id="aace3-102">手順 5: DataControl を使用可能な状態にする (RDS チュートリアル)</span><span class="sxs-lookup"><span data-stu-id="aace3-102">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>


<span data-ttu-id="aace3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="aace3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aace3-p101">返された **Recordset** オブジェクトは、利用可能な状態です。他の **Recordset** と同様に、調査、移動、または編集を行うことができます。 **Recordset** に対して実行できる操作は、環境によって異なります。Visual Basic および Visual C++ には、直接的に、またはデータ コントロールを使って間接的に **Recordset** を使用できる、ビジュアル コントロールがあります。</span><span class="sxs-lookup"><span data-stu-id="aace3-p101">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="aace3-108">たとえば、Microsoft Internet Explorer で、web ページを表示している場合はビジュアル コントロールに**レコード セット**オブジェクトのデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="aace3-108">For example, if you are displaying a webpage in Microsoft Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="aace3-109">Web ページのビジュアル コントロールは、**レコード セット**オブジェクトに直接アクセスできません。</span><span class="sxs-lookup"><span data-stu-id="aace3-109">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="aace3-110">しかし、 **DataControl (RDS)** を通じて [Recordset](datacontrol-object-rds.md) にアクセスすることはできます。</span><span class="sxs-lookup"><span data-stu-id="aace3-110">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="aace3-111">**RDS.DataControl** は、その [SourceRecordset](recordset-sourcerecordset-properties-rds.md) プロパティが **Recordset** オブジェクトに設定されている場合に、ビジュアル コントロールによって使用可能な状態になります。</span><span class="sxs-lookup"><span data-stu-id="aace3-111">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="aace3-112">ビジュアル コントロール オブジェクトの **DATASRC** パラメーターは **RDS.DataControl** に、 **DATAFLD** プロパティは **Recordset** オブジェクトのフィールド (列) に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="aace3-112">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="aace3-113">このチュートリアルでは、 **SourceRecordset** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="aace3-113">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

