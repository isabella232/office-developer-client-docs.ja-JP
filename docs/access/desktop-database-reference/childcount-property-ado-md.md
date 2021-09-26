---
title: ChildCount プロパティ (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0e52bd6cb6296fa8409658892f68d2ab2aefeda4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618526"
---
# <a name="childcount-property-ado-md"></a>ChildCount プロパティ (ADO MD)


**適用先**: Access 2013、Office 2013

階層内で、現在の [Member](member-object-ado-md.md) オブジェクトが親であるメンバーの数を示します。

## <a name="return-values"></a>戻り値

長整数型 (**Long**) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

**ChildCount** プロパティを使用して、 **Member** が持つ子の数の概算を取得します。 **Member** の子自体は、 [Children](children-property-ado-md.md) プロパティを使用して取得します。

**Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトから取得される値は、最大で 65536 です。子の実際の数が 65536 を超える場合でも、取得される値は 65536 となります。そのため、 **ChildCount** が 65536 である場合、アプリケーションは子の数が 65536 または以上であると解釈する必要があります。

**Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトの場合、ADO コレクションの [Count](count-property-ado.md) プロパティを **Children** コレクションに使用して、子の正確な数を調べます。コレクション内にある子の数が多い場合、子の正確な数を確認するのに時間がかかることがあります。

