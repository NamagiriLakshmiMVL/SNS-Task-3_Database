# 1.MongoDB Schema for Project Data

const mongoose = require("mongoose");

const projectSchema = mongoose.Schema(
{
name: { type: String, required: true },
description: { type: String, required: true },
startDate: { type: Date, required: true },
endDate: { type: Date, required: true },
id: { type: Number, required: true },
technologies: { type: Array },
},
{ timestamps: true }
);

const projectModel = mongoose.model("PROJECTS", projectSchema);
module.exports = projectModel;

---

# 2.MongoDB Schema for Storing User Information

const mongoose = require("mongoose");

const userSchema = mongoose.Schema(
{
name: { type: String, required: true },
email: { type: String, required: true },
password: { type: String, required: true },
},
{ timestamps: true }
);

const userModel = mongoose.model("projectUsers", userSchema);
module.exports = userModel;
