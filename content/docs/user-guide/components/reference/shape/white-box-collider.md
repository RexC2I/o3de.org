---
description: ' Use the White Box Collider component to add PhysX collision to white
  box meshes in Open 3D Engine. '
title: 'White Box Collider component'
---




You can enable collision on white box meshes in O3DE by adding the **White Box Collider** component to an entity that has a **White Box** component mesh. The **White Box Collider** component supports collision layers and physics materials. It can be used with static and kinematic white box meshes. The **White Box Collider** component uses the white box mesh as the collision surface. Unlike the **PhysX Collider** component, there is no need to specify a collision shape or provide a PhysX mesh asset.

![White Box static collider.](/images/user-guide/component/whitebox/white-box-collider-A.gif)

In the animation above, the **White Box Collider** component is applied to a static **White Box** component. The **White Box** component can be edited and the changes tested for collision immediately.

![White Box kinematic collider.](/images/user-guide/component/whitebox/white-box-collider-B.gif)

In the animation above, the door was created with White Box and animated with a script. Note When the **White Box** component is edited, the **White Box Collider** component automatically recognizes the changes to the mesh. You can then test the changes immediately.

## White Box Collider properties 

![White Box Collider component interface.](/images/user-guide/component/whitebox/ui-white-box-collider.png)

****Collision Layer****
The collision layer that's assigned to the collider. For more information, see [Collision Layers](/docs/user-guide/interactivity/physics/nvidia-physx/configuring/configuration-collision-layers/).

****Collides With****
The collision group containing the layers that this collider collides with. For more information, see [Collision Groups](/docs/user-guide/interactivity/physics/nvidia-physx/configuring/configuration-collision-groups/).

****Physics Material - Library****
Set the physics material library for this collider.

****Physics Material - Mesh Surfaces****
Choose a material from the physics material library for this collider. The material is applied to the entire white box entity.

****Tag****
Set a tag for this collider. Tags can be used to quickly identify components in script or code.

****Body Type****
Select **Static** for non-moving entities. Select **Kinematic** for animated entities.
The White Box collider must be set to **Static** to interact with the **PhysX Character Controller**.
