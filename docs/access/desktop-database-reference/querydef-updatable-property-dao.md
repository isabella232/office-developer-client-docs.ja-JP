---
title: QueryDef プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303333"
---
# <a name="querydefupdatable-property-dao"></a>QueryDef プロパティ (DAO)


**適用先:** Access 2013、Office 2013

DAO オブジェクトを変更できるかどうかを示す値を返します。 値の取得のみ可能なブール型 (**Boolean**) の値です。

## <a name="syntax"></a>構文

*式*。できる

*式***QueryDef**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

クエリ結果の **[Recordset](recordset-object-dao.md)** オブジェクトを更新できないときでも、クエリ定義を更新できる場合、**QueryDef** オブジェクトの **Updatable** プロパティは **True** に設定されます。

