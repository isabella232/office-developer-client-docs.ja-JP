---
title: Recordset2 プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b6e6f2a20b4779259b80eff1fc152abe3698217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309325"
---
# <a name="recordset2updatable-property-dao"></a>Recordset2 プロパティ (DAO)


**適用先:** Access 2013、Office 2013

DAO オブジェクトを変更できるかどうかを示す値を返します。 値の取得のみ可能なブール型 (**Boolean**) の値です。

## <a name="syntax"></a>構文

*式*。できる

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

スナップショットタイプおよび前方スクロールタイプの Recordset オブジェクトでは、常に**False**が返されます。

オブジェクトの種類の中には、更新できないフィールドが含まれている場合がよくあります。たとえば、一部のフィールドしか変更できないようなダイナセット タイプの **Recordset** オブジェクトを作成することもできます。これらのフィールドは固定にすることも、自動的に増加するデータを含めることもでき、また更新可能なテーブルと更新できないテーブルを組み合わせたクエリによってダイナセットを得ることもできます。

オブジェクトに読み取り専用フィールドしか含まれていない場合、 **Updatable** プロパティの値は **False** となります。1 つ以上のフィールドが更新可能な場合、このプロパティの値は **True** となります。更新可能なフィールドのみ編集できます。新しい値を読み取り専用フィールドに割り当てると、トラップ可能なエラーが発生します。

更新可能なオブジェクトには読み取り専用フィールドが含まれていることがあるため、レコードを編集する前に、 **Recordset** オブジェクトの **Fields** コレクションの各フィールドの **DataUpdatable** プロパティを確認する必要があります。

