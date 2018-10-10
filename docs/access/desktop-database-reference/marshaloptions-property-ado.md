---
title: MarshalOptions プロパティ (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478758"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="55bd0-102">MarshalOptions プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="55bd0-102">MarshalOptions Property (ADO)</span></span>


<span data-ttu-id="55bd0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="55bd0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="55bd0-104">どのレコードがサーバーにマーシャリングされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="55bd0-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="55bd0-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="55bd0-105">Settings And Return Values</span></span>

<span data-ttu-id="55bd0-p101">[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。</span><span class="sxs-lookup"><span data-stu-id="55bd0-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55bd0-108">解説</span><span class="sxs-lookup"><span data-stu-id="55bd0-108">Remarks</span></span>

<span data-ttu-id="55bd0-p102">クライアント側の [Recordset](recordset-object-ado.md) を使用する場合、クライアントで修正されたレコードは、マーシャリングという技術により、中間層または Web サーバーに書き戻されます。マーシャリングとは、スレッドまたはプロセスの境界を越えてインターフェイス メソッドのパラメーターをパッケージ化して送信するプロセスです。 **MarshalOptions** プロパティを設定すると、修正されたリモート データをマーシャリングして中間層や Web サーバーを更新するときのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="55bd0-p102">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries. Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</span></span>

<span data-ttu-id="55bd0-111">**リモート データ サービスの使用法**このプロパティはクライアント側の**Recordset**でのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="55bd0-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

