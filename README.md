# ![LOGO](logo.png) Custom Vision Training Client **flow**ground Connector

## Description

A generated **flow**ground connector for the Custom Vision Training Client API (version 2.2).

Generated from: https://api.apis.guru/v2/specs/microsoft.com/cognitiveservices-Training/2.2/swagger.json<br/>
Generated at: 2019-05-07T17:43:03+03:00

## API Description



## Authorization

This API does not require authorization.

## Actions

### Get a list of the available domains.

*Tags:* `DomainsApi`

#### Input Parameters
* `Training-Key` - _required_

### Get information about a specific domain.

*Tags:* `DomainsApi`

#### Input Parameters
* `domainId` - _required_ - The id of the domain to get information about.
* `Training-Key` - _required_

### Get your projects.

*Tags:* `ProjectApi`

#### Input Parameters
* `Training-Key` - _required_

### Create a project.

*Tags:* `ProjectApi`

#### Input Parameters
* `name` - _required_ - Name of the project.
* `description` - _optional_ - The description of the project.
* `domainId` - _optional_ - The id of the domain to use for this project. Defaults to General.
* `classificationType` - _optional_ - The type of classifier to create for this project.
    Possible values: Multiclass, Multilabel.
* `Training-Key` - _required_

### Delete a specific project.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Get a specific project.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The id of the project to get.
* `Training-Key` - _required_

### Update a specific project.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The id of the project to update.
* `Training-Key` - _required_

### Delete images from the set of training images.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `imageIds` - _required_ - Ids of the images to be deleted. Limited to 256 images per batch.
* `Training-Key` - _required_

### Add the provided images to the set of training images.

> This API accepts body content as multipart/form-data and application/octet-stream. When using multipart<br/>
> multiple image files can be sent at once, with a maximum of 64 files

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `tagIds` - _optional_ - The tags ids with which to tag each image. Limited to 20.
* `Training-Key` - _required_

### Add the provided batch of images to the set of training images.

> This API accepts a batch of files, and optionally tags, to create images. There is a limit of 64 images and 20 tags.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Get images by id for a given project iteration.

> This API will return a set of Images for the specified tags and optionally iteration. If no iteration is specified the<br/>
> current workspace is used.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `imageIds` - _optional_ - The list of image ids to retrieve. Limited to 256.
* `iterationId` - _optional_ - The iteration id. Defaults to workspace.
* `Training-Key` - _required_

### Add the specified predicted images to the set of training images.

> This API creates a batch of images from predicted images specified. There is a limit of 64 images and 20 tags.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Delete a set of image regions.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `regionIds` - _required_ - Regions to delete. Limited to 64.
* `Training-Key` - _required_

### Create a set of image regions.

> This API accepts a batch of image regions, and optionally tags, to update existing images with region information.<br/>
> There is a limit of 64 entries in the batch.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Get tagged images for a given project iteration.

> This API supports batching and range selection. By default it will only return first 50 images matching images.<br/>
> Use the {take} and {skip} parameters to control how many images to return in a given batch.<br/>
> The filtering is on an and/or relationship. For example, if the provided tag ids are for the "Dog" and<br/>
> "Cat" tags, then only images tagged with Dog and/or Cat will be returned

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _optional_ - The iteration id. Defaults to workspace.
* `tagIds` - _optional_ - A list of tags ids to filter the images. Defaults to all tagged images when null. Limited to 20.
* `orderBy` - _optional_ - The ordering. Defaults to newest.
    Possible values: Newest, Oldest.
* `take` - _optional_ - Maximum number of images to return. Defaults to 50, limited to 256.
* `skip` - _optional_ - Number of images to skip before beginning the image batch. Defaults to 0.
* `Training-Key` - _required_

### Gets the number of images tagged with the provided {tagIds}.

> The filtering is on an and/or relationship. For example, if the provided tag ids are for the "Dog" and<br/>
> "Cat" tags, then only images tagged with Dog and/or Cat will be returned

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _optional_ - The iteration id. Defaults to workspace.
* `tagIds` - _optional_ - A list of tags ids to filter the images to count. Defaults to all tags when null.
* `Training-Key` - _required_

### Remove a set of tags from a set of images.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `imageIds` - _required_ - Image ids. Limited to 64 images.
* `tagIds` - _required_ - Tags to be deleted from the specified images. Limited to 20 tags.
* `Training-Key` - _required_

### Associate a set of images with a set of tags.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Get untagged images for a given project iteration.

> This API supports batching and range selection. By default it will only return first 50 images matching images.<br/>
> Use the {take} and {skip} parameters to control how many images to return in a given batch.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _optional_ - The iteration id. Defaults to workspace.
* `orderBy` - _optional_ - The ordering. Defaults to newest.
    Possible values: Newest, Oldest.
* `take` - _optional_ - Maximum number of images to return. Defaults to 50, limited to 256.
* `skip` - _optional_ - Number of images to skip before beginning the image batch. Defaults to 0.
* `Training-Key` - _required_

### Gets the number of untagged images.

> This API returns the images which have no tags for a given project and optionally an iteration. If no iteration is specified the<br/>
> current workspace is used.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _optional_ - The iteration id. Defaults to workspace.
* `Training-Key` - _required_

### Add the provided images urls to the set of training images.

> This API accepts a batch of urls, and optionally tags, to create images. There is a limit of 64 images and 20 tags.

*Tags:* `ImageApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Get iterations for the project.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Delete a specific iteration of a project.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _required_ - The iteration id.
* `Training-Key` - _required_

### Get a specific iteration.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The id of the project the iteration belongs to.
* `iterationId` - _required_ - The id of the iteration to get.
* `Training-Key` - _required_

### Update a specific iteration.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - Project id.
* `iterationId` - _required_ - Iteration id.
* `Training-Key` - _required_

### Get the list of exports for a specific iteration.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _required_ - The iteration id.
* `Training-Key` - _required_

### Export a trained iteration.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _required_ - The iteration id.
* `platform` - _required_ - The target platform.
    Possible values: CoreML, TensorFlow, DockerFile, ONNX.
* `flavor` - _optional_ - The flavor of the target platform.
    Possible values: Linux, Windows, ONNX10, ONNX12.
* `Training-Key` - _required_

### Get detailed performance information about an iteration.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The id of the project the iteration belongs to.
* `iterationId` - _required_ - The id of the iteration to get.
* `threshold` - _optional_ - The threshold used to determine true predictions.
* `overlapThreshold` - _optional_ - If applicable, the bounding box overlap threshold used to determine true predictions.
* `Training-Key` - _required_

### Get image with its prediction for a given project iteration.

> This API supports batching and range selection. By default it will only return first 50 images matching images.<br/>
> Use the {take} and {skip} parameters to control how many images to return in a given batch.<br/>
> The filtering is on an and/or relationship. For example, if the provided tag ids are for the "Dog" and<br/>
> "Cat" tags, then only images tagged with Dog and/or Cat will be returned

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _required_ - The iteration id. Defaults to workspace.
* `tagIds` - _optional_ - A list of tags ids to filter the images. Defaults to all tagged images when null. Limited to 20.
* `orderBy` - _optional_ - The ordering. Defaults to newest.
    Possible values: Newest, Oldest.
* `take` - _optional_ - Maximum number of images to return. Defaults to 50, limited to 256.
* `skip` - _optional_ - Number of images to skip before beginning the image batch. Defaults to 0.
* `Training-Key` - _required_

### Gets the number of images tagged with the provided {tagIds} that have prediction results from<br/>
> training for the provided iteration {iterationId}.

> The filtering is on an and/or relationship. For example, if the provided tag ids are for the "Dog" and<br/>
> "Cat" tags, then only images tagged with Dog and/or Cat will be returned

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _required_ - The iteration id. Defaults to workspace.
* `tagIds` - _optional_ - A list of tags ids to filter the images to count. Defaults to all tags when null.
* `Training-Key` - _required_

### Delete a set of predicted images and their associated prediction results.

*Tags:* `PredictionsApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `ids` - _required_ - The prediction ids. Limited to 64.
* `Training-Key` - _required_

### Get images that were sent to your prediction endpoint.

*Tags:* `PredictionsApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Quick test an image.

*Tags:* `PredictionsApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _optional_ - Optional. Specifies the id of a particular iteration to evaluate against.
            The default iteration for the project will be used when not specified.
* `Training-Key` - _required_

### Quick test an image url.

*Tags:* `PredictionsApi`

#### Input Parameters
* `projectId` - _required_ - The project to evaluate against.
* `iterationId` - _optional_ - Optional. Specifies the id of a particular iteration to evaluate against.
            The default iteration for the project will be used when not specified.
* `Training-Key` - _required_

### Get the tags for a given project and iteration.

*Tags:* `TagsApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `iterationId` - _optional_ - The iteration id. Defaults to workspace.
* `Training-Key` - _required_

### Create a tag for the project.

*Tags:* `TagsApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `name` - _required_ - The tag name.
* `description` - _optional_ - Optional description for the tag.
* `type` - _optional_ - Optional type for the tag.
    Possible values: Regular, Negative.
* `Training-Key` - _required_

### Delete a tag from the project.

*Tags:* `TagsApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `tagId` - _required_ - Id of the tag to be deleted.
* `Training-Key` - _required_

### Get information about a specific tag.

*Tags:* `TagsApi`

#### Input Parameters
* `projectId` - _required_ - The project this tag belongs to.
* `tagId` - _required_ - The tag id.
* `iterationId` - _optional_ - The iteration to retrieve this tag from. Optional, defaults to current training set.
* `Training-Key` - _required_

### Update a tag.

*Tags:* `TagsApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `tagId` - _required_ - The id of the target tag.
* `Training-Key` - _required_

### Queues project for training.

*Tags:* `ProjectApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `Training-Key` - _required_

### Get region proposals for an image. Returns empty array if no proposals are found.

> This API will get region proposals for an image along with confidences for the region. It returns an empty array if no proposals are found.

*Tags:* `ImageRegionProposalApi`

#### Input Parameters
* `projectId` - _required_ - The project id.
* `imageId` - _required_ - The image id.
* `Training-Key` - _required_

## License

**flow**ground :- Telekom iPaaS / microsoft-com-cognitiveservices-training-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
