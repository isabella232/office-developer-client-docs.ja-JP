---
title: OLE �Y�t�t�@�C��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b95b83ad7eedff577e4c36365c9e451f4b458173
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801668"
---
# <a name="ole-attachments"></a><span data-ttu-id="381b3-103">OLE �Y�t�t�@�C��</span><span class="sxs-lookup"><span data-stu-id="381b3-103">OLE Attachments</span></span>

  
  
<span data-ttu-id="381b3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="381b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="381b3-p101">OLE �I�u�W�F�N�g�́AOLE 1 �Ƃ��ăG���R�[�h�́A�Y�t�t�@�C���́A�I�u�W�F�N�g�̉��ʌ݊�����X�g���[�~���O���܂��B�{���Ɍ��̃I�u�W�F�N�g�� OLE 2 **IStorage**�I�u�W�F�N�g�̏ꍇ�́A�I�u�W�F�N�g�� OLE 1 �X�g���[���ɕϊ�����K�v������܂��BWin32 OLE ���C�u�����̈ꕔ�ł��� **OleConvertIStorageToOLESTREAM** �֐���g�p���Ă��̕ϊ������s����܂��B</span><span class="sxs-lookup"><span data-stu-id="381b3-p101">Attachments that are OLE objects are encoded as OLE 1 stream objects for backward compatibility. If the original object is really an OLE 2 **IStorage** object, then the object must be converted to an OLE 1 stream. This conversion is performed using the **OleConvertIStorageToOLESTREAM** function, which is part of the Win32 OLE libraries.</span></span> 
  

