---
title: TableDef.ValidationText プロパティ (DAO)
TOCTitle: ValidationText Property
ms:assetid: 9f38616a-41ee-cbd1-9e29-da436b258e08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198366(v=office.15)
ms:contentKeyID: 48546682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c45aa1bd6f470b342ffec51f2affd39c7cb552
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710483"
---
# <a name="tabledefvalidationtext-property-dao"></a><span data-ttu-id="35eec-102">TableDef.ValidationText プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="35eec-102">TableDef.ValidationText property (DAO)</span></span>


<span data-ttu-id="35eec-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="35eec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35eec-p101">**Field** オブジェクトの値が **ValidationRule** プロパティの設定に設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="35eec-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="35eec-106">構文</span><span class="sxs-lookup"><span data-stu-id="35eec-106">Syntax</span></span>

<span data-ttu-id="35eec-107">*式*です。ValidationText</span><span class="sxs-lookup"><span data-stu-id="35eec-107">*expression* .ValidationText</span></span>

<span data-ttu-id="35eec-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="35eec-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="35eec-109">注釈</span><span class="sxs-lookup"><span data-stu-id="35eec-109">Remarks</span></span>

<span data-ttu-id="35eec-110">**[TableDef](tabledef-object-dao.md)** オブジェクトの場合、このプロパティの設定値は、リンク テーブルでは取得のみ可能で、ベース テーブルでは、取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="35eec-110">For a **[TableDef](tabledef-object-dao.md)** object, this property setting is read-only for a linked table and read/write for a base table.</span></span>

