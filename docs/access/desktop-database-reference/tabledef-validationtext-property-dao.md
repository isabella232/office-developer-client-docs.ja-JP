---
title: ValidationText プロパティ (DAO)
TOCTitle: ValidationText Property
ms:assetid: 9f38616a-41ee-cbd1-9e29-da436b258e08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198366(v=office.15)
ms:contentKeyID: 48546682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c45aa1bd6f470b342ffec51f2affd39c7cb552
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314246"
---
# <a name="tabledefvalidationtext-property-dao"></a><span data-ttu-id="6016f-102">ValidationText プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6016f-102">TableDef.ValidationText property (DAO)</span></span>


<span data-ttu-id="6016f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6016f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6016f-p101">**Field** オブジェクトの値が **ValidationRule** プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="6016f-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6016f-106">構文</span><span class="sxs-lookup"><span data-stu-id="6016f-106">Syntax</span></span>

<span data-ttu-id="6016f-107">*式*。ValidationText</span><span class="sxs-lookup"><span data-stu-id="6016f-107">*expression* .ValidationText</span></span>

<span data-ttu-id="6016f-108">\*式\***TableDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="6016f-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6016f-109">注釈</span><span class="sxs-lookup"><span data-stu-id="6016f-109">Remarks</span></span>

<span data-ttu-id="6016f-110">**[TableDef](tabledef-object-dao.md)** オブジェクトの場合、このプロパティの設定値は、リンク テーブルでは取得のみ可能で、ベース テーブルでは、取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="6016f-110">For a **[TableDef](tabledef-object-dao.md)** object, this property setting is read-only for a linked table and read/write for a base table.</span></span>

